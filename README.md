Docker container for AWS DynamoDB Local

AWS DynamoDB Local will let you test against DynamoDB without needing
a full network. For details see https://aws.amazon.com/blogs/aws/dynamodb-local-for-desktop-development/

To use link to your application:

    sudo docker run -d --name dynamodb deangiberson/aws-dynamodb-local

    sudo docker run -d -P --name web --link dynamodb:dynamodb training/webapp python app.py
