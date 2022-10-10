Reference Page;
```
https://awscli.amazonaws.com/v2/documentation/api/latest/index.html
```
for configuration:
```
aws configure set aws_access_key_id=$AWS_ACCESS_KEY_ID aws_secret_access_key=$AWS_SECRET_ACCESS_KEY --region=us-east-1 --output=json
```

* to set the configuration but it writes under the line again, not to overwrite
```
aws configure list-profiles
```
to list;
```
aws configure list 
```
gives output like;
```
    Name                    Value             Type    Location
      ----                    -----             ----    --------
   profile                <not set>             None    None
access_key     ****************NZ5R shared-credentials-file
secret_key     ****************8dxX shared-credentials-file
    region                us-east-1      config-file    ~/.aws/config
```
to set identity;
```
aws sts get-caller-identity   #it gives default profile info.
```

or can be used;
```
aws sts get-caller-identity --profile <profile-name>  # it shows the specific profile..
```

gives output like;
```
{
    "UserId": "xxxxxxxxxxxxxxxxx",
    "Account": "xxxxxxxxxxxxxx",
    "Arn": "arn:aws:iam::xxxxxxxxxxxx:user/fikret"
}
```
