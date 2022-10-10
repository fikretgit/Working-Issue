reference page;
```
https://aws.amazon.com/tr/premiumsupport/knowledge-center/s3-configure-cors/

https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManageCorsUsing.html
```

samples;

[{
    "AllowedHeaders": [
        "*"
    ],
    "AllowedMethods": [
        "PUT",
        "POST",
        "DELETE"
    ],
    "AllowedOrigins": [
        "http://www.example.com"
    ],
    "ExposeHeaders": [
        "x-amz-server-side-encryption",
        "x-amz-request-id",
        "x-amz-id-2"
    ],
    "MaxAgeSeconds": 3000
}]

we can arrange it like;

[{
    "AllowedHeaders": [
        "*"
    ],
    "AllowedMethods": [
        "*",
    ],
    "AllowedOrigins": [
        "*"
    ],
    "ExposeHeaders": [
        "*"
    ],
    "MaxAgeSeconds": 3000
}]