# actions-workflows
Helpful Custom Workflows used by Lunar Drift


## S3 Sync 
How to Use:
```yaml
on:
  push:
    branches:
      - main

jobs:
  s3_sync:
    runs-on: ubuntu-latest
    steps:
    - uses: lunar-drift/actions-workflows/.github/workflows/s3-sync.yaml@main
      with:
        bucket_name: "your-bucket-name"
        # optional inputs
        # dir_to_sync: "."
        # aws_region: "eu-west-1"
      secrets:
        AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
        AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}

```
