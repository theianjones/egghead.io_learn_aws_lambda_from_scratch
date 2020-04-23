# Add logs to AWS Lambda function and review them in CloudWatch

[Video link](https://egghead.io/lessons/aws-add-logs-to-aws-lambda-function-and-review-them-in-cloudwatch?pl=learn-aws-lambda-from-scratch-d29d)

You can `console.log` in your functions and, when executing from the console, these are easy to find. However, when accessed through the API Gateway, these logs are captured by AWS logging service, CloudWatch.

CloudWatch is how you view the logs of your lambda triggers. For our function it provides several log streams. Clicking on the newest one will show our logging message.

Every execution of our lambda logs the following basics to CloudWatch:

- When the function starts
- When the function ends
- Report of the execution time of the function
