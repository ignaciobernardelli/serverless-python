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
