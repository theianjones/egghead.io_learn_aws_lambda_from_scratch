# List all S3 buckets from an AWS Lambda function using aws-sdk

[Video link](https://egghead.io/lessons/aws-list-all-s3-buckets-from-an-aws-lambda-function-using-aws-sdk?pl=learn-aws-lambda-from-scratch-d29d)

We can require the `aws-sdk` without uploading it as a dependency.

This lets us interact with other services in the AWS ecosystem.

```js
const s3 = new AWS.S3();
const myBuckets = await s3.listBuckets().promise();

console.log(myBuckets);
```

This will give an access denied error as AWS works on a [principle of least priviledge](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#grant-least-privilege) model.

We can add the correct permissions by clicking `Permissions` at the top and then the role name (something like `myS3Function-role-lnzh95co`). This will bring us to the IAM console, AWS identity management platform.

From here we can attach policies, search for S3 and add the `ReadOnlyAccess`.

The function will now work. It is good practice to follow AWS examples and only grant the privileges that are strictly needed.
