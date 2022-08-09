# Authorisation and Authentication demo for FE module

The `start` branch is your jumping off point, a simple React app has been created consisting of a `home`, `account` and `login` pages.

Here we will solve the problems of:
- authenticating a user,
- having to re-authenticate when refreshing the page / leaving and returning to the site through the use of cookies
- using bcryptjs to encrypt the password and ensure better security

The desired behaviour is for the user to be shown the `account` page when they are logged in, otherwise they should be redirected to the `login` component when trying clicking the `account` link.
At this starting point, this behaviour is hard-coded as the app has no knowledge of the authenticated status of the user (as it hasn't been created yet!)

The app does not use a back end for authentication, for the purposes of demonstrating the mechanics and workflow a fake login process is used which will mimic the response of a real API (in the case of JWT, by returning an an authentication token). See `utils/fakeLogin.js`

## Packages used
- dotenv
- jsonwebtoken
- jwt-decode
- js-cookie
- react test renderer
- bcryptjs

## Installation and checking out branches

### Branch structure
There are 3 branches:
- `start`
This is the starting point, consisting of the basic app as described at the top of this file.

- `jwt-solution`
This is the solution building on the start branch that implements `jwt`, `jsonwebtoken` and `js-cookies` to persist a users authentication status between refreshes

- `bcrypt-with-jwt`
This builds on the `jwt-solution` branch, adding `bcryptjs` to create a hash of a users password and compare the entered password with the hash when a user attempts to login

### Installation
Clone down this repo and run `npm install`. Checkout the `start` branch to try and create the solution yourself, or checkout the relevant solution branch to see an implementation.

### Checking out branches
To checkout a branch you do not have locally but is present on the remote repository, use command `git checkout -t origin/branchname-here`, or once you have the branches locally use `git switch branchname-here`.

## Available scripts
- `npm start`
- `npm test`
