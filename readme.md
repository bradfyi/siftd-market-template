# Google Cloud

- project: ```siftd-k8s-dogfood```

- ```
gcloud artifacts repositories create siftd-market-template-repo \
    --project=siftd-k8s-dogfood \
    --repository-format=docker \
    --location=us-west1 \
    --description="Docker repository for Marketing Template"
```

- repo: ```siftd-market-template-repo```

```
gcloud builds submit \
  --tag us-west1-docker.pkg.dev/siftd-k8s-dogfood/siftd-market-template-repo/siftd-market-template-gke .
```