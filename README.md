# Copy Git Repository to S3
Simple GitHub action to copy all Git files to S3

## AWS IAM Policy

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "ObjectActionBucket",
            "Effect": "Allow",
            "Action": [
                "s3:PutObject",
                "s3:GetObject"
            ],
            "Resource": [
                "arn:aws:s3:::<BUCKET_NAME>/*"
            ]
        },
        {
            "Sid": "ListBucket",
            "Effect": "Allow",
            "Action": [
                "s3:ListBucket"
            ],
            "Resource": [
                "arn:aws:s3:::<BUCKET_NAME>"
            ]
        }
    ]
}
```
