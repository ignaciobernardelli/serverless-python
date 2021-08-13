## RUN

```
docker build -t serverless-python -f Dockerfile .

docker run --env PORT=5000 -it -p 80:5000 serverless-python
```

## Push
### Via Docker

```
docker build -t serverless-python -f Dockerfile .

docker tag serverless-python gcr.io/glossy-radio-321418/serverless-python

docker push gcr.io/glossy-radio-321418/serverless-python
```

## Via Gcloud Build

```
gcloud builds submit --tag gcr.io/glossy-radio-321418/serverless-python-2 .
```


## Deploy

```
gcloud run deploy serverless-python --image gcr.io/glossy-radio-321418/serverless-python-2 --platform managed --region us-west1 
```