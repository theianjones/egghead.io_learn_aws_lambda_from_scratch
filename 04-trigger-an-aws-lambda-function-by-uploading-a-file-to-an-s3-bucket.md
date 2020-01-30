# Trigger an AWS Lambda function by uploading a file to an S3 bucket

You can trigger your function when someone updates an S3 bucket

- add s3 trigger

And `event` is passed to the lambda function.

S3 event has a `event.records` array on it.
