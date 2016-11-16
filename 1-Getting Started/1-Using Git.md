# Get the boilerplate and set up base files

```
cd <project dir>
git clone git@github.com:NukaSRB/JumpGate.git ./
composer install
cp .env.example .env
php artisan key:generate
yarn
gulp
php artisan vendor:publish --provider="JumpGate\Core\Providers\ViewServiceProvider"
```

At this point, your site will display the JumpGate home page.  From here on out, you will customize as you normally would.

1. Set up your database in the .env file
    * Run `php artisan migrate` afterwards to test and get the migrations table going.
