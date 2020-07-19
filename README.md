# dvc-mlflow-e2e-example




### 

Step-by-step guide: 

1. Init and set up DVC

```
dvc init
```

Put bucket credentials 

```
cat c:\Users\<user>\.aws\credentials

[default]
aws_access_key_id=***
aws_secret_access_key=****
```

Configure s3 bucket (or use minio):

```
dvc remote add -d s3remote s3://dvc/imdb-e2e
```

Configure bucket host name (optional)

```
dvc remote modify s3remote endpointurl <YOUR URL TO BUCKET>
```

