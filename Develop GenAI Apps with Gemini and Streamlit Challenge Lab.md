
## Develop GenAI Apps with Gemini and Streamlit Challenge Lab [GSP517]

## Task 2
```
wine = st.radio(
          "What wine do you prefer?\n\n", ["Red", "white", "None"], key="wine", horizontal=True
        )
```


```
PROJECT='Enter your project id'
REGION='Enter your region'

python3 -m venv gemini-streamlit
source gemini-streamlit/bin/activate
python3 -m pip install -r requirements.txt
streamlit run chef.py --browser.serverAddress=localhost --server.enableCORS=false --server.enableXsrfProtection=false --server.port 8080
```
## Task 3 & 4
```
vi Dockerfile
```

### change file name chef.py

```
AR_REPO='chef-repo'
SERVICE_NAME='chef-streamlit-app'
gcloud artifacts repositories create "$AR_REPO" --location "$REGION" --repository-format=Docker
gcloud builds submit --tag "$REGION-docker.pkg.dev/$PROJECT/$AR_REPO/$SERVICE_NAME"
gcloud run deploy "$SERVICE_NAME" --port=8080 --image="$REGION-docker.pkg.dev/$PROJECT/$AR_REPO/$SERVICE_NAME" --allow-unauthenticated --region=$REGION --platform=managed --project=$PROJECT --set-env-vars=PROJECT=$PROJECT,REGION=$REGION
```

##  Thanks !!
