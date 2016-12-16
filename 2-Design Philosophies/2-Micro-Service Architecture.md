# Micro-Service Architecture
 
- [Introduction](#introduction)
- [Set Up](#set-up)
    - [Manual](#set-up-manual)
    - [Commands](#set-up-commands)
- [Naming Conventions](#naming-conventions)
 
<a name="introduction"></a>
## Introduction
Micro-service architecture is a name we have given to our newest way of organizing code.  The concept here is to break up 
the app into services.  Each service should contain all of its own needs such as models, controllers, routes, events, 
etc.  The service will end up looking like a miniature app or a small package in the end, and this is what we are wanting 
to see.  The benefits of this are that all the code you need for the service is inside a single directory and easy to 
find.  It also allows working for client to be smoother as you can work based on services with clearly defined needs and 
a built in stopping point to push, stage and demo.

<a name="set-up"></a>
## Set Up
<a name="set-up-manual"></a>
### Manually
To begin with services, create a `Services` folder in your `app` directory if one doesn't exist already.  Inside that folder 
you should place any of the following folders you may need.

```
- Commands
- Contracts
- Events
- Http
    - Controllers
    - Routes
- Jobs
- Listeners
- Models
- Repositories
- Transformers
```

Events, Http, Http/Controllers, Listeners and Models all behave exactly the same as their app level counterparts.  Commands 
is where you would place any commands.  These are the special jobs we have that are fired and forgotten about using 
the `command()` helper.  Contracts would be where you place all of your interface files.  Http/Routes is the location for 
your class based routes.  Repositories would be where repositories go should you need them.  Transformers is the location 
of the transformer files used to make sure the view and vue files have consistent data at all times.  These could also be 
used for APIs.

<a name="set-up-commands"></a>
### Commands
This section will be written once the commands are completed.

<a name="naming-conventions"></a>
## Naming Conventions
For consistency the following rules should be observed.

1. You MUST name your service as a verb when possible.
    - `Incentivizing` instead of `Incentives`.
1. You SHOULD NOT add the type of class to the name.
    - The Incentive controller should be called `Incentive` and not `IncentiveController`.
1. You MUST use singular names for your controllers.
    - `Incentive` and not `Incentives`.
1. You MUST keep resource route names singular.
    - This is for consistency and to avoid confusion in spelling.
