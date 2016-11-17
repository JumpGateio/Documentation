# Set up

- []()

## Introduction
In this walk through we will be building a simple blog app starting with JumpGate.  It really should not take too long so 
feel free to follow along.

During this walkthrough I will be assuming you are using the prerequisites listed below and your set up using valet.  If you 
 are using homestead or something else, modify the valet sections to suit your environment.

## Prerequisites
- yarn
    - `npm install -g yarn`
- [composer](https://getcomposer.org/download/)
- [Homebrew](http://brew.sh/)
- PHP/MySql
    - [Homestead](https://laravel.com/docs/5.3/homestead)
    - [Valet](https://laravel.com/docs/5.3/valet)
        - `brew update`
        - `brew install homebrew/php/php70`
        - `brew install php70-xdebug`
        - `brew install mariadb`
        - `composer global require laravel/valet`
        - `valet install`
    - [Sequel Pro](https://www.sequelpro.com/)
- [JumpGateInstaller](https://github.com/NukaSRB/Installer)
    - `composer global require jumpgate/installer`

## Installation

First, go make the directory you want your projects to live in.  I use `~/Code/` but use anything you want.

In your terminal go into that directory (`cd ~/Code`).  Now we will bring in JumpGate.  Run `jumpgate new Blog` and let the installer do its 
thing.  This will bring in JumpGate with [Core](https://github.com/NukaSRB/Core), [Menu](https://github.com/NukaSRB/Menu), 
[Admin](https://github.com/NukaSRB/Admin) and [Users](https://github.com/NukaSRB/Users).  Everything we need to start up a blog.

Once it finished, go into your new project (`cd Blog/`) and run `valet park`.  This will let valet start sharing the 
directory.  And speaking of, you should now be able to browse to `http://blog.dev` and see the JumpGate homepage!
 
## Database

With installation out of the way, lets look to the database.  Since we will need one we should work on the design that we 
will need and get teh database set up.

Open up sequel pro and set up a connection to localhost.  It should have a host of `127.0.0.1`, a username of `root` and 
that's it.  Save and connect to the host and click the "Choose database..." drop down to select "Add Database".  Name it 
"blog" and click "Add".  That's it!

In your project, open `.env` and add the database details as follows.

```
DB_CONNECTION="mysql"
DB_HOST="127.0.0.1"
DB_PORT=3306
DB_DATABASE="blog"
DB_USERNAME="root"
DB_PASSWORD=""
```

Next run `php artisan migrate`.
