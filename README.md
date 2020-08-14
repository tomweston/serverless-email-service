# Serverless Email Service

A simple lambda that takes in a name, message and email address.  Sends an email to your desired mailbox.

Unique emails are saved to DynamoDB, emails can only be submitted once per week per address.

### Usage

Install Serverless, [follow the installation instructions here](https://www.serverless.com/framework/docs/providers/aws/guide/installation/). Requires at least version v1.26 or later as that's the version that comes with Golang support. 

To deploy run

```serverless deploy```

There is only one enpoint ```/sendMail```.  

It requires a body consisting of:
```json
{
    "name": "String",
    "email": "String",
    "message": "String"
}
```
