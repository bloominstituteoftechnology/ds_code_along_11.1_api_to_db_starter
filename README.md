# spotify_search

The purpose of this code along is to practice: 

- Taking in user input from a form.
- Querying a third party API based on the user input. 
- Processing the API response and storing the response data to a custom database table.
- Querying the database and displaying the results on a webpage.

The structure of this project and the pieces you will be filling in with the (help of your instructor) are are similar to what you will have to do on the Sprint Challenge. Plus, you'll get to make the beginnings of a cool music recommendation app! We'll take this project even further in the next code along. 

### Startup Instructions

1) Clone the repository and change directories so that you're working from the outer project folder (ds_code_along_11.1_api_to_db_starter).

2) Ensure that all dependencies are properly installed:

 `pipenv install`

3) Activate the virtual enviroment:

`pipenv shell`

4) Sign up for a [Spotify Developer Account.](https://developer.spotify.com/dashboard/login) Get a `CLIENT_ID` and `CLIENT_SECRET` and assign those api keys to their corresponding environment variables in the `.env` file 

Your final .env file should look something like this:

```
FLASK_ENV=development
CLIENT_ID=18886d8afa9b48aa3282286d88bd7bb
CLIENT_SECRET=a337e9d27034923adf9ccd319459750
```

but with your own personal CLIENT_ID and CLIENT_SECRET. The API Keys shown in the above example will *NOT* work.

4) Change directories to `spotify_app`:

 `cd spotify_app`
 
5) Add contents to the `app.py` file (right now this file is completely blank). We'll work on filling it in with your instructure during the Code-Along.

6) When you're ready, you can start up the app with the following command;

`FLASK_APP=app.py flask run`

7) The first time that you launch the app and visit the home page: `localhost:5000' the app will likely throw an error. This is because the database and database tables have not been generated. Make sure that your app has a `/reset` route that you can visit to trigger the creation of the DB and any associated tables. 

Your `/reset` route might look something like this:

```python
@app.route('/reset')
def reset():
    DB.drop_all()
    DB.create_all()
    return render_template('base.html')
```

Try visiting [the reset route](localhost:5000/reset) first to create the DB and DB tables and then your app should run like normal (if there aren't any other errors). Once the database file has been generated once it will not need to be regenerated in the future unless it gets deleted. Once you have visited the reset route one time, you should be able to return to the home page and use the app normally. 
