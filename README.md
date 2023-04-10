# Cohesive GitHub Action
> _Simple & optimized static sites_

## Example S3 Deployment

```yaml
name: Deploy
on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: aws-actions/configure-aws-credentials@v2
        with:
          role-to-assume: "arn:aws:iam::123456890:role/deploy-role"
      - uses: cohesiveio/action@v0
        with:
          storage: s3
          bucket: webapp-bucket
```
