---
description: "Configuration of proj-frontiers dev deployment"
title: jpa05-proj-frontiers
nav_order: 100
parent: lab/jpa05
layout: default
---

# {{page.title}} - {{page.description}}


## Step 2: Configure your app for localhost as documented in the README.md

### 2a: Google OAuth Setup

Assuming that you have set up a project in the Google Developer Console and set up an OAuth Consent Screen for your project (which should have been done in `jpa03`), you will just need to create a set of OAuth credentials (`GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` values) using Steps 1-4 of these instructions: [Oauth Google Setup](https://ucsb-cs156.github.io/topics/oauth/oauth_google_setup.html) 

**NOTE:** The name of your Dokku app for `jpa05` will be `dining-dev-yourGithubUsername`, so your Dokku redirect URI will be <tt>https://<b><i>dining-dev-yourGithubUsername</i></b>.dokku-<b><i>xx</i></b>.cs.ucsb.edu/login/oauth2/code/google</tt>, where <i>xx</i> is your team number.

Then, complete Step 1 in [oauth.md](https://github.com/ucsb-cs156/proj-courses/blob/main/docs/oauth.md) (set up `.env` values for `localhost`, including `ADMIN_EMAILS` and `UCSB_API_KEY`)

### 2b: Github OAuth Setup

TODO: Add link to instructions for Github OAuth setup.


### 2c: Launch your application

* Open *two separate terminal windows*  
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

Then, the app should be available on <http://localhost:8080>. Test that Oauth was set up properly by logging in. 


## Step 3: Configure your app to run on Dokku


## Return to the main instructions

Please return to the main instructions 
for information on submitting.
