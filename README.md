# DPCRAS3CF

Github Action what **d**e**p**loying **CRA** app at AWS **S3** and **C**loud**F**ront

_It is not limited to CRA app, just customize some command_

## How to use it

1. Customize trigger

```yml
on: # trigger when push to master
    push:
        branches:
            - master
```

2. Add Option

```yml
jobs:
    deploy:
        runs-on: ubuntu-18.04 #or -latest
        env:
            AWS_S3_BUCKET_NAME: your-s3-bucket-name
            AWS_CF_DISTRIBUTION_ID: your-cloudfront-distribution_id
            AWS_REGION: your-s3-region-name
            # and you need github secrets for
            # ASW_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY
```

3. Add Secrets at your repo

```yml
${{ secrets.AWS_ACCESS_KEY_ID }}
${{ secrets.AWS_SECRET_ACCESS_KEY }}
```

## More info with korean

[Check my blog post](https://www.hyesungoh.xyz/React/cdS3CfWithGithubAction/)
