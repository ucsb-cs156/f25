---
description: "Configuration of proj-courses dev deployment"
title: jpa05-proj-courses
nav_order: 100
parent: lab/jpa05
layout: default
---

# {{page.title}} - {{page.description}}


## Step 2: Configure your app for localhost as documented in the README.md
First, complete step 1 of oauth setup here:
* <https://github.com/ucsb-cs156/proj-courses/blob/main/docs/oauth.md>
  
Next, follow the steps here to configure a UCSB API key:
* <https://ucsb-cs156.github.io/topics/apis/apis_ucsb_developer_api.html>

Open *two separate terminal windows*
* In the first window, start up the backend with:
  ``` 
  mvn spring-boot:run
  ```
* In the second window:
  ```
  cd frontend
  npm install  # only on first run or when dependencies change
  npm start
  ```

Then, the app should be available on <http://localhost:8080>
     
## Step 3: Configure your app to run on Dokku
Next, you need to create a personal dokku deployment so that you can test future PRs during the legacy code project. 

Name the app `courses-dev-yourGithubUsername` and follow the steps here: 
* <https://ucsb-cs156.github.io/topics/dokku/deploying_an_app.html>

You also need to configure MONGODB_URI in the .env file, following the instructions here: 

* <https://github.com/ucsb-cs156/proj-courses/blob/main/docs/mongodb.md>

And lastly, you need to configure the value of CHROMATIC_PROJECT_TOKEN, following the instructions here: 
* <https://ucsb-cs156.github.io/topics/chromatic/#what-is-chromatic>


## Return to the main instructions

Please return to the main instructions 
for information on submitting.
