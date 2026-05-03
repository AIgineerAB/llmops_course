# Deploy dockerized RAG application to Azure

<a href="https://youtu.be/Y789Ur0X9kg" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/ai_engineering/rag_lllmops_5.png?raw=true" alt="rag deployment to azure" width="600">
</a>


## MLFlow container 

Startup command in Azure container app 

```bash
mlflow, server, --host, 0.0.0.0, --port, 5000, --backend-store-uri, sqlite:////mlflow/mlflow.db, --allowed-hosts, *
```

environment variable 

```
MLFLOW_SERVER_CORS_ALLOWED_ORIGINS=*
```

## Backend container

Push the image to Azure container registry 

```
docker buildx build --platform linux/amd64 --provenance=false -f dockerfiles/backend.dockerfile -t <ACR_LOGIN_SERVER>/ragnimal-backend:v1 --push .
```

When creating the container app you need to put in the following environment variables

- COHERE_API_KEY=
- GEMINI_API_KEY=
- OPENROUTER_API_KEY=
- MLFLOW_TRACKING_URI=<MLFLOW_URL>
- GIT_PYTHON_REFRESH=quiet

## Frontend container

Push the image to Azure container registry 

```
docker buildx build --platform linux/amd64 --provenance=false -f dockerfiles/frontend.dockerfile -t <ACR_LOGIN_SERVER>/ragnimal-frontend:v1 --push .
```

- API_URL=<BACKEND_URL>




## Read more


## Other videos