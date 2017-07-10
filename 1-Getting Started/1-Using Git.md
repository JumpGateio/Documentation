# Get the boilerplate and set up base files

```
cd <project dir>
git clone git@github.com:JumpGateio/JumpGate.git ./
composer install
cp .env.example .env
php artisan key:generate
yarn
npm run dev
```

> If you want to include users, use git@github.com:JumpGateio/JumpGate-Users.git for the clone.

At this point, your site will display the JumpGate home page.  From here on out, you will customize as you normally would.

1. Set up your database in the .env file
    * Run `php artisan migrate` afterwards to test and get the migrations table going.
