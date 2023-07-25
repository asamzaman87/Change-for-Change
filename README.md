# Change-for-Change
Change for Change is an application which rounds up a user's expenses, collects them, and then donates them to an organization of the user's choice.

## Setup
### Download Code
Open up your IDE and open the terminal. Copy and paste the command below

`git clone https://github.com/alival000/Change-for-Change.git`

Follow the prompts and save the resulting folder in the directory that you want.

Open the folder in your IDE to create a new project

### Download the Requirements and Database
Run the following command to download all requirements into your virtual environment

`pip install -r requirements.txt`

This will download the framework and all other APIs needed to run the webapp

#### Database
PostgresSQL is a database system. Install the latest version of PostgreSQL [here](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads)
Follow the prompts to install the database.

pgAdmin is an interface to view your Postgres database.
Install the latest version of pgAdmin [here](https://www.pgadmin.org/download/) and follow the prompts
to install the application. Make sure to make your password **"abc123"**

Open up pgAdmin. Open up the Server tab on the left-hand side. Right click on Databases and add a new database called _ChangeForChange_ , and _BankAPI_

Go to `/migrate` endpoint while the server is running in the browser to run all SQL files and initialize your database

Go to `/migrate_bank` endpoint while the server is running in the browser to run all SQL files and initialize your bank database

_Note: If psycopg2 is throwing an error, enter `pip install postgres` into your terminal_

### How to Commit New Code

    1. git add .
    2. git commit -m "[enter your message here]"
    3. git pull
    4. git push

#### Step 1

The first step is to add your changes. To check all the files you changed/added/deleted, run the following command:

`git status`

This will list all of you changed files. If you want to only add changes from a specific file use the following command:

`git add filename.txt`

If you want to add all of your changes, use the following command:

`git add .`

You can use `git status` again to check that the files you have added are under the _Changes to be committed_ group

#### Step 2
 
The next thing you want to do is package your changes to be sent to the repository. Use the command below:

`git commit -m "[enter your message here]"`

This will start your commit. the `-m` flag means you are attaching a message, _which is required for all commits_. 
Replace the `[enter your message here]` with a short message on the content of your changes

#### Step 3

Once your changes are committed, you can pull changes from the repository online. This can be done with the command below:

`git pull`

Once changes are pulled in, you will be able to see the most recent version of the repository in your IDE

#### Step 4

The final step is to push your changes to the repository. This can be done with the command below:

`git push`

If it is asking you for a username and password, enter your github username and a personal access token. 

_Note: If you want to skip the credential check, you can log into github on your IDE or set up an SSH token. 
Then you won't be prompted to enter credentials during every push_

#### Example

    1. git add homepage.html
    2. git commit -m "added new homepage"
    3. git pull
    4. git push

## Pytest

To run pytest, type the following command into your terminal

`pytest`

This will run the unit tests and show the results