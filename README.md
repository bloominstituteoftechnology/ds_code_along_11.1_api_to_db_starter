# spotify_search

The purpose of this code along is to practice: 

- Taking in user input from a form.
- Querying a third party API based on the user input. 
- Processing the API response and storing the response data to a custom database table.
- Querying the database and displaying the results on a webpage.

The structure of this project and the pieces you will be filling in with the (help of your instructor) are are similar to what you will have to do on the Sprint Challenge. Plus, you'll get to make the beginnings of a cool music recommendation app! We'll take this project even further in the next code along. 

### Startup Instructions

#### STEP 1 - Clone the repository and change directories so that you're working from the outer project folder (ds_code_along_11.1_api_to_db_starter).

#### STEP 2 - Ensure that all dependencies are properly installed:

 `pipenv install`

#### STEP 3 - Activate the virtual enviroment:

`pipenv shell`

#### STEP 4 - Sign up for a [Spotify Developer Account.](https://developer.spotify.com/dashboard/login) Get a `CLIENT_ID` and `CLIENT_SECRET` and assign those api keys to their corresponding environment variables in the `.env` file 

Your final .env file should look something like this:

```
FLASK_ENV=development
CLIENT_ID=18886d8afa9b48aa3282286d88bd7bb
CLIENT_SECRET=a337e9d27034923adf9ccd319459750
```

but with your own personal CLIENT_ID and CLIENT_SECRET. The API Keys shown in the above example will *NOT* work.

#### STEP 5 - Change directories to `spotify_app`:

 `cd spotify_app`

#### STEP 6 - Run the App

`FLASK_APP=app.py flask run`

The app will not load properly until you have added contents to the app.py file. We will be filling in the contents of this file together during the code-along. If you want to see if you can get things running before the code-along begins (not required). You can try following the [Flask Quickstart Guide](https://flask.palletsprojects.com/en/1.1.x/quickstart/) to set up a basic app.py file:

```python
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello, World!'
```
