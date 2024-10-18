sam-static-website

This project contains source code and supporting files for a serverless application that you can deploy with the SAM CLI.


Run the next commands

``` 
sam package --template-file template.yaml --s3-bucket <your-s3-bucket> --output-template-file packaged.yaml
``` 

```
sam deploy --template-file packaged.yaml --stack-name sam-static-website --capabilities CAPABILITY_IAM
``` 

Upload the website to the s3 bucket

``` 
aws s3 sync ./website s3://<your-s3-bucket-name> --acl public-read
``` 
