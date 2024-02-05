# cloudbuild-test
Google Cloudbuild test

Enable APIs:
gcloud services enable artifactregistry.googleapis.com --project=lazlo-python-test

Create Docker Repository:
gcloud artifacts repositories create docker-repo \
    --repository-format=docker \
    --location=europe-west1 \
    --project=lazlo-python-test

gcloud services enable cloudbuild.googleapis.com --project=lazlo-python-test
gcloud services enable secretmanager.googleapis.com --project=lazlo-python-test

Create cloud build repository link manually on the console
Create coudbuild trigger manually ont he console

gcloud services enable container.googleapis.com --project lazlo-python-test
Create manually a GKE cluster

