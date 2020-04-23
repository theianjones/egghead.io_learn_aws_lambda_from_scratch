# Add an API Gateway trigger to a AWS Lambda function to create a REST API

[Video link](https://egghead.io/lessons/aws-add-an-api-gateway-trigger-to-a-aws-lambda-function-to-create-a-rest-api?pl=learn-aws-lambda-from-scratch-d29d)

Without an API Gateway, our function can only be triggered inside of the console.

In the lambda console:

Add trigger -> API Gateway -> HTTP API

For now, set the security to open. That's fine for now but will need to be reviewed going live.

Once back in the console, we'll see our API Gateway including the endpoint. Clicking on this will show our "Hello from Lambda!" message.

Updates in the function will be immediately accessible to this endpoint.
