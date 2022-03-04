# Multiple firebase environments - CRA App.

## Firebase setup:

- Set up two firebase projects, one for dev/staging and the second for production.
- The default project is prfetably the dev/staging env.

## Directory setup:

- Dev dependency: `react-app-env` required to handle multiple environment variables for multiple projects.
- `staging.env` file holds the firebase config for **staging** project.
- `production.env` file holds the firebase config for **production** project.

View `package.json`

## NPM Scripts:

```
"build:staging": "react-app-env --env-file=staging.env build",
"build:production": "react-app-env --env-file=production.env build",
"deploy:staging": "npm run build:staging && firebase use default && firebase deploy",
"deploy:production": "npm run build:production && firebase use production && firebase deploy"
```
