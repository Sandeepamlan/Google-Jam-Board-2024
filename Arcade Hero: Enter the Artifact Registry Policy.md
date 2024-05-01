## Arcade Hero: Enter the Artifact Registry Policy [ARC157]



# Processing state for new CoMManD

```

export REPO_NAME=prod-registry

export REGION=us-east1

gcloud artifacts repositories create $REPO_NAME --repository-format=docker --location=$REGION

```
