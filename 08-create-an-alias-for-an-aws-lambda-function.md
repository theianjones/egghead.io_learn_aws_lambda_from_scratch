# Create an alias for an AWS Lambda function

[Video link](https://egghead.io/lessons/aws-create-an-alias-for-an-aws-lambda-function?pl=learn-aws-lambda-from-scratch-d29d)

The `ARN` in the top right corner is the `Amazon Resource Name` for that lambda function.

Actions -> create alias

This is a way you can test different versions of your function.

Weights can be assigned to each version based on percentage of traffic.

Lets you A/B test your functions.

You can change which resource the alias is pointing to which allows us to update the functions without changing the code that is calling it.
