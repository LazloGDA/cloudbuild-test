# Google Cloudbuild test

## Enable APIs:
gcloud services enable artifactregistry.googleapis.com --project=lazlo-python-test
gcloud services enable cloudbuild.googleapis.com --project=lazlo-python-test
gcloud services enable secretmanager.googleapis.com --project=lazlo-python-test
gcloud services enable container.googleapis.com --project lazlo-python-test
gcloud services enable container.googleapis.com --project lazlo-python-test

## Steps for auto build push and deploy this test-app 

Create Docker Repository:

gcloud artifacts repositories create docker-repo \
    --repository-format=docker \
    --location=europe-west1 \
    --project=lazlo-python-test

Create cloud build repository link manually on the console

Create coudbuild trigger manually on the console

Create a GKE autopilot cluster:

gcloud container clusters create-auto sample-cluster --location=europe-west1 --project=lazlo-python-test

Another role was needed to deploy a not existing workload:

gcloud projects add-iam-policy-binding lazlo-python-test --member=serviceAccount:690547025497@cloudbuild.gserviceaccount.com --role=roles/container.developer



