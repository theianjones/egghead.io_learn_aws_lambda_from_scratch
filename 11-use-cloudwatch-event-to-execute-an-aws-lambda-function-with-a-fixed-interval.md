# Use CloudWatch event to execute an AWS Lambda function with a fixed interval

[Video link](https://egghead.io/lessons/aws-use-cloudwatch-event-to-execute-an-aws-lambda-function-with-a-fixed-interval?pl=learn-aws-lambda-from-scratch-d29d)

You can add CloudWatch event as a trigger to a function

This is how you can run function on a timer.

Add trigger->CloudWatch Event->Rule

You can use a Cron or rate expression to schedule when this will be triggered.

```
rate(1 minute)
```

vs

```
0 * 0 ? * * *
```
