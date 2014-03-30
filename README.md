<h1>README</h1>

Welcome to the Card Collection Manager application. The purpose of this application to allow trading card collection owners to easily manage their trading card collections online.

How to setup the application:

* make sure you set up the secret key for your rails application

* make sure you set up the database.yml file for your rails application

<h2>Set up the secret key for rails</h2>

The project is configured using the dotenv gem to manage appication environment variables. You won't be able to run the rails server until you give your application a 'SECRET_KEY_BASE'. This is loaded in the file /config/initializers/secret_token.rb

To set this variable, execute the command <tt>rake secret</tt> in your command line. This will generate a random key string. Create a .env file in the root project directory, and include this line: 

<tt>SECRET_KEY_BASE=(yoursecretkeyhere)</tt>

<h2>Set up the database.yml</h2>

The project by default uses the postgresql gem to persist data. Create a file in your /config directory called database.yml and include your database configuration details. An example looks like this:

```
development:
  adapter: postgresql
  database: my_dev_db
  pool: 5
  timeout: 5000

test:
  adapter: postgresql
  database: my_test_db
  pool: 5
  timeout: 5000
```
