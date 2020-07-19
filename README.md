# dvc-mlflow-e2e-example

## Data Source 

The original dataset was taken from http://ai.stanford.edu/~amaas/data/sentiment/

```
This is a dataset for binary sentiment classification containing substantially more data than previous benchmark datasets. We provide a set of 25,000 highly polar movie reviews for training, and 25,000 for testing. There is additional unlabeled data for use as well. Raw text and already processed bag of words formats are provided. See the README file contained in the release for more details.
```

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
