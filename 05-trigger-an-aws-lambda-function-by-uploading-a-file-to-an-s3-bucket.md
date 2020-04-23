# Trigger an AWS Lambda function by uploading a file to an S3 bucket

[Video link](https://egghead.io/lessons/aws-trigger-an-aws-lambda-function-by-uploading-a-file-to-an-s3-bucket?pl=learn-aws-lambda-from-scratch-d29d)

You can trigger your function when someone updates an S3 bucket.

Create the function and from the console, Add Trigger->S3.

You'll need to have already created an S3 bucket for this. To do that, go to the Services->S3->Create bucket and name the bucket. These names have to be globally unique. You can click the refresh icon beside the bucket list to see your new bucket.

The trigger can be further configured to only care about particular prefixes (in other places we'd call those folders but S3 doesn't have `folders` even though it looks like they do) or suffixes (file types for example).

And `event` is passed to the lambda function. You can create a test S3 object from the test menu `Event Template` - the `Amazon S3 Put` is particularly userful.

S3 event has a `event.Records` array on it - we can log the s3 details like this:

```js
console.log("event", event.Records[0].s3);
```

This will log the details, either of our test event or any file that is uploaded to our bucket.
