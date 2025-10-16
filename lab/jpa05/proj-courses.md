---
description: "Configuration of proj-courses dev deployment"
title: jpa05-proj-courses
nav_order: 100
parent: lab/jpa05
layout: default
---

# {{page.title}} - {{page.description}}


## Step 2: Configure your app for localhost as documented in the README.md

In this step, you are configuring your app to run on localhost.  This consists mainly 
of:
* Copying `.env.SAMPLE` to `.env`
* Filling in various values in the `.env` as explained below.

Two values you will NOT need to set for this assignment are:
* `CHROMATIC_PROJECT_TOKEN` (we'll need this later, but not now)
* `MONGODB_URI` (we'll need to set this on dokku, but not localhost)

First, complete step 1 of oauth setup here:
* <https://github.com/ucsb-cs156/proj-courses/blob/main/docs/oauth.md>

Next, follow the steps here to configure a UCSB API key:
* <https://ucsb-cs156.github.io/topics/apis/apis_ucsb_developer_api.html>

Open *two separate terminal windows*, each of which has the directory where you cloned the repo as the current directory.

* In the first window, start up the backend with:
  ``` 
  mvn spring-boot:run
  ```
* In the second window, start up the frontend with:
  ```
  cd frontend
  nvm install 20.17.0
  nvm use 20.17.0
  npm install  # only on first run or when dependencies change
  npm start
  ```

Then, the app should be available on <http://localhost:8080>
     
## Step 3: Configure your app to run on Dokku
Next, you need to create a personal dokku deployment so that you can test future PRs during the legacy code project. 

Name the app `courses-dev-yourGithubUsername` and follow the steps here: 

* <https://ucsb-cs156.github.io/topics/dokku/deploying_an_app.html>

You also need to set up MongoDB on Dokku, following the instructions here: 

* <https://github.com/ucsb-cs156/proj-courses/blob/main/docs/mongodb.md>

## Return to the main instructions

Please return to the main instructions 
for information on submitting.
