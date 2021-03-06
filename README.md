# Game-Card - Full Stack FastAPI and Vue.js - MongoDB Deploy Heroku

**Host: https://game-card-watcharapon.herokuapp.com**
****

Generate a backend and frontend stack using Python, including interactive API documentation.

**Interactive API documentation**
![Alt text](https://github.com/watcharap0n/game-card/blob/main/static/Screen%20Shot%202564-03-26%20at%2001.25.57.png?raw=true "Title")

**Feature**

    - Python FastAPI backend:
        - Fast: Very high performance, on par with NodeJS and Go (thanks to Starlette and Pydantic).
        - Intuitive: Great editor support. Completion everywhere. Less time debugging.
        - Easy: Designed to be easy to use and learn. Less time reading docs.
        - Short: Minimize code duplication. Multiple features from each parameter declaration.
        - Robust: Get production-ready code. With automatic interactive documentation.
        - Standards-based: Based on (and fully compatible with) the open standards for APIs: OpenAPI and JSON Schema.
        - Many other features including automatic validation, serialization, interactive documentation, authentication with OAuth2 JWT tokens, etc.
    - Firebase Authentication
    - WebSocket Pusher
    - Vue frontend Generated with Vue CDN and Vuetify
    - Database MongoDB
    - Docker Compose Local

`Create and activate a virtual environment`

`Config Vars`

- MONGODB_URI
- GOOGLE_CREDENTIALS
- GOOGLE_APPLICATION_CREDENTIALS

`add buildpack`

- heroku/python
- https://github.com/elishaterada/heroku-google-application-credentials-buildpack

~~~~
$ python3 -m venv venv && source venv/bin/activate
 ~~~~        

`Project Setup`

~~~~
pip install -r requirements.txt
 ~~~~

`Web Server`

~~~~
(venv)$ uvicorn main:app --reload --workers 2 --host 0.0.0.0 --port 8080
~~~~

`Run Serve`

~~~~
Python app.py
 ~~~~

`Setup MongoDB`

~~~~
- brew tap mongodb/brew
- brew install mongodb-community@4.4
- brew install --cask robo-3t
 ~~~~

`Run Database`

~~~~
sudo mongod --dbpath /usr/local/var/mongodb
 ~~~~

`Deploy Heroku`

~~~~
$ heroku login
$ heroku git:clone -a game-card-watcharapon
$ cd game-card-watcharapono
$ git add .
$ git commit -am "make it better"
$ git push heroku master
 ~~~~
