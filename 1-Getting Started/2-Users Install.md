# Users Install

- [Commands](#commands)

<a name="commands"></a>
## Installation

```
cd <project dir>
git clone git@github.com:JumpGateio/JumpGate-Users.git ./
composer install
cp .env.example .env
php artisan key:generate
yarn
npm run dev
```

At this point, your site will display the JumpGate home page.  From here on out, you will customize as you normally would.

1. Set up your database in the `.env` file
1. Update your `configs/jumpgate/users.php` file to detail how you want users to be set up.

```
php artisan migrate
php artisan db:seed --class=UserStatuses
php artisan db:seed --class=UserRoles
```
