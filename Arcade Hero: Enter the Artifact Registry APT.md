## Arcade Hero: Enter the Artifact Registry APT [ARC154]

```
export REPO_NAME=prod-registry

export REGION=us-central1

gcloud artifacts repositories create $REPO_NAME --repository-format=apt --location=$REGION

```
