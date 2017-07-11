# Base Install

- [Commands](#commands)
- [Users](#users)

<a name="commands"></a>
## Installation

```
cd <project dir>
git clone git@github.com:JumpGateio/JumpGate.git ./
composer install
cp .env.example .env
php artisan key:generate
yarn
npm run dev
```
At this point, your site will display the JumpGate home page.  From here on out, you will customize as you normally would.

1. Set up your database in the `.env` file
1. Run `php artisan migrate`.

<a name="users"></a>
## Users

If your site will need users you have 3 choices here.  

1. Install the [JumpGate-Users repository](/2-Users-Install.md) instead.
1. Run through [adding users](/3-Add-Users-to-Base-Install.md) to a base JumpGate installation.
1. Create your own users system.