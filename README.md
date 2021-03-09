# Gentics Angular Challenge

# How to get started

Hi, and welcome to the Angular Challenge! Please fork this repo, and clone for yourself.

After a quick `npm install` you can start the stack by running `npm start`.

Your frontend will running on http://localhost:4200 and the backend part is proxied via /api. See the API endpoints documented here later.

Hint: There are no validations from the backend side at all, so any data will be accepted from you requests.
## Goals
**Create a simple password manager using only the following API endpoints.**

Create a simple password manager using only the following API endpoints.

A user should enter the "Master Password" which is the secret ID in that case. For simplicity only use "gentics" for that, which is pre-added to the backend. Check if the provided secret exists and list the available credentials.

Allow users to create new credentials and delete others.

You can use other libraries for the frontend to achieve the goal.

* Please use only the provided API endpoints from this README
* It's a frontend test, you don't have to consider the security measurements of the backend logic
* Do as much as you can in 1 hour and push a commit
* You can continue after that if you would like to
## API:

Checking if secret exists:
```
GET http://localhost:4200/api/pwdb/:pwdbId
```

Should return: `{"id:":":pwdbID"}`

Fetching all credetials of a secret:
```
GET http://localhost:4200/api/pwdb/:pwdbId/credentials
```

Fetching a single credential of a secret:
```
GET http://localhost:4200/api/pwdb/:pwdbId/credentials?id=:credentialId
```

Creating a new credential for a secret:
```
POST http://localhost:4200/api/pwdb/:pwdbId/credentials
```

Example Body:
```json
{
  "name": "New credential",
  "username": "testuser",
  "password": "123456"
}
```

Deleting a credential for a secret:
```
DELETE http://localhost:4200/api/credentials/:credentialId
```

---

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.2.3.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
