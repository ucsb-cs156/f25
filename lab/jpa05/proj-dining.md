---
description: "Configuration of proj-dining dev deployment"
title: jpa05-proj-dining
nav_order: 100
parent: lab/jpa05
layout: default
---

# {{page.title}} - {{page.description}}


## Step 2: Configure your app for localhost (as documented in the README.md)

# 2a

First, you will need a value for `UCSB_API_KEY`; you can obtain a value for that by following the instructions at this link: <https://ucsb-cs156.github.io/topics/apis/apis_ucsb_developer_api.html>

# 2b

Then, before running the application for the first time, do the steps documented in [`docs/oauth.md`](docs/oauth.md).

Otherwise, when you try to login for the first time, you will likely see an error such as:

<img src="https://user-images.githubusercontent.com/1119017/149858436-c9baa238-a4f7-4c52-b995-0ed8bee97487.png" alt="Authorization Error; Error 401: invalid_client; The OAuth client was not found." width="400"/>

# 2c

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

Then, the app should be available on <http://localhost:8080>


## Step 3: Configure your app to run on Dokku


## Return to the main instructions

Please return to the main instructions 
for information on submitting.
