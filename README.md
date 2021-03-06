# Google Speech to Text and sentiment analysis

Using Google STT API with text-processing.com Sentiment Analysis API

### Google Documentation

https://cloud.google.com/speech/docs/getting-started
https://cloud.google.com/iam/docs/service-accounts
https://developers.google.com/identity/protocols/application-default-credentials

### Create a STT Project in Google Console

1. Go to Project Credentials page:  
https://console.developers.google.com/projectselector/apis

2. Create new project and give it a name. Make a note of the **Project ID**. 

3. You should automatically be asked to create credentials now. Choose the Service Account Key, add any Service Account Name and choose the Role of Project > Owner. Download the JSON credentials file.
![Create crednetials](http://recordit.co/ULWuLVcJXi.gif)
_DO NOT LOOSE THIS FILE_

4. Copy the downloaded JSON file into the `scripts/` directory.

5. Enable Speech to Text API for this project. Be sure to select the project that you just created in the drop down menu
https://console.developers.google.com/apis/api/speech.googleapis.com/overview

![Enable API](http://recordit.co/bO7Nvp9llM.gif)


## Install all node dependencies
```
npm install
```

### Setup envvar file

In terminal:
```
cd _REPLACE_WITH_PROJECT_PATH_/scripts/
chmod +x setup.sh
./setup.sh
source envvar
```

### Change Project ID
In `app.js`:
```
var date = new Date()
var recordPath = "recordings/" + date.getTime() +".wav";
const projectId = 'your-project-id-goes-here';
```

### Run script...and talk
```
node app.js
```
