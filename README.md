# wp-local

Purpose of this repo is to have a boilerplate WordPress Docker install.

## Services
1. MySQL
2. PHPMyAdmin
3. Webserver

## Instructions
### Files
Download a zip of this repo and place it into any directory in your 
project.  We usually use `./local` placed in the root of the project.

Ignore this folder in your `.gitignore`.

### Docker Build
Run `cd ./local/` then `docker-compose build`.

### Install Wordpress
Download and copy the latest version of WP into the current directory.

### Running
While still in the `local` directory, run `docker-compose up` to launch 
the services.

This will run a WP server running on `http://localhost` port 80, and 
PHPMyAdmin on port 8080.

### Installing Wordpress
With the WordPress files in place and your `docker-compose up` running, 
navigate to http://localhost.

Internally we change our hosts to have more specific host names:

```
127.0.0.1 wordpress-test-site.test
```

#### Go through the installation process.  Use the following values for 
setting up the local instance:
**hostname:** `db`
**database:** `wordpress`
**username:** `wordpress`
**password:** `wordpress`

_Note: The `database`, `username` and `password` can all be customized on 
the **docker-compose.yml** file.  Do not change the `hostname`_
