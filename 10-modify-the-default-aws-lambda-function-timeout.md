# Modify the default AWS Lambda function timeout

[Video Link](https://egghead.io/lessons/aws-modify-the-default-aws-lambda-function-timeout?pl=learn-aws-lambda-from-scratch-d29d)

When you scroll down, you can modify the time out and memory usage of the function. By default, the timeout is 3 seconds and can be increased up to 15 minutes.

You can also set the memory.

To see how long we have left before the timeout, we can access a helper function from the context object.

```js
context.getRemainingTimeInMillis();
```
