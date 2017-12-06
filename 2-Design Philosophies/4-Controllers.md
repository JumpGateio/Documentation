# Controllers

- [Naming](#naming)
- [Method Conventions](#method-conventions)

<a name="naming"></a>
## Naming
There are a few rules we follow when it comes to controllers.

1. When the controller is inside a service, it MUST NOT contain the word controller in its file name.
1. When the controller is in the base (app/Http/Controllers) directory, it MAY contain the word controller.
1. Controller names MUST be singular.

<a name="method-conventions"></a>
## Method Conventions
In order to keep the code clean, readable and non-monolithic, keep these rules in mind.

> [This is a great video](https://www.youtube.com/watch?v=MF0jFKvS4SI) on this subject.

1. Use only the standard 7 resourceful actions on a controller.
  - If you can't fit what you are trying to do into the following actions.
    - Index
    - Show
    - Create
    - Store
    - Edit
    - Update
    - Destroy
1. If your action doesn't fit in these standard 7, make a new controller in which it does fit.
