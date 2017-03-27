# aws-lambda-mongodb-backup
A NodeJS project that demonstrates how to make a backup file of a MongoDB database and store the file in a S3 bucket. This project is designed to be executed as an AWS Lambda function.

## Build

```
npm install --save
```

## Test

Then, test the Lambda function with a test event using the following environment variables:

```json
{
  "MONGODB_URL": "yourDatabaseURL",
  "MONGODB_DB": "demo",
  "MONGODB_USER": "demo",
  "MONGODB_PASSWORD": "password",
  "S3_BUCKET": "myBucket",
  "AWS_KEY": "accessKey", --> (not used if not in local mode)
  "AWS_SECRET_KEY": "secretAccessKey" --> (not used if not in local mode)
}
```
## Usage in AWS
Zip the project and upload it in your AWS Lambda function.

## To Do's:
- Simplify the code for cleaning up a backup file
- Handle irregular error from cleaning up a backup file
- Accept more than 1 MongoDB reaplica IP addresses
- Any other error handling logic

