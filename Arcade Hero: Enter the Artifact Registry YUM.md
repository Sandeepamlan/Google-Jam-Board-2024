## Arcade Hero: Enter the Artifact Registry YUM [ARC155]

```
export REPO_NAME=prod-registry

export REGION=us-central1

gcloud artifacts repositories create $REPO_NAME --repository-format=yum --location=$REGION

```
