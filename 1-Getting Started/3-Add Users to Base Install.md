# Add Users to Base Install

- [Introduction](#introduction)
- [Files](#files)

<a name="introduction"></a>
## Introduction

This document assumes you created a [base JumpGate](/1-Base-Install.md) site and now want to add in users.  To get started 
open up [the Users build](https://github.com/JumpGateio/InstallerBuilds/tree/Users/Users/5.4) in a new window.  This will 
contain all the files we will need to add.

<a name="files"></a>
## Files

All we have to do now is move the files from the repository into our app.  If you have modified any of these files already, 
just take the parts needed for users and bring it into your version of the file.


File | Install To | Important Parts
---- | ---------- | ----------------
AuthServiceProvider.php | `app/Providers/AuthServiceProvider.php` | The foreach in the boot method and the `getPermissions()` method.
Kernel.php | `app/Http/Kernel.php` | The `active` and `acl` middlewares.
MenuComposer.php | `app/Http/Composers/MenuComposer.php` | [Optional] The auth links inside `generateRightMenu()`.
RouteServiceProvider.php | `app/Providers/RouteServiceProvider.php` | The User Routes in the providers array.
User.php | `app/Models/User.php` | Required for users to work.  Will be created automatically after you register the UserServiceProvider in app.php.
app.php | `config/app.php` | Adding `JumpGate\Users\Providers\UsersServiceProvider::class` and `Kodeine\Acl\AclServiceProvider::class` to the provides array.
users.php | `config/jumpgate/users.php` | Whole file.  Used to determine how the users package will run.
acl.php | `config/acl.php` | Whole file.  Used to configure the acl details.
