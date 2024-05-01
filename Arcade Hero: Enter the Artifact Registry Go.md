## Arcade Hero: Enter the Artifact Registry Go [ARC156]

```
export REPO_NAME=prod-registry

export REGION=us-east1

gcloud artifacts repositories create $REPO_NAME --repository-format=go --location=$REGION

```
