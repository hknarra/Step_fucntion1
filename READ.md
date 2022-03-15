# Create State machine with a simple Lambda fucntion.

## Create Lambda function with below code:
### handler.py
```
def hello(event, context):
    print("2nd change")
    return "hello"
```
### serverless.yml file
```
service: hello-world-python-2

frameworkVersion: '2'

provider:
  name: aws
  runtime: python3.8
  lambdaHashingVersion: 20201221
  profile: <profile name here>
  region: us-east-1


functions:
  hello:
    handler: handler.hello
```
