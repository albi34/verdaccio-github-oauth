# sinopia-github-oauth
Sinopia authentication plugin with github oauth web flow

This will allow you to auth via github web oauth flow. It is compatible with [sinopia2](https://www.npmjs.com/package/sinopia2)

## Installation
* Create an [oauth application](https://github.com/settings/applications/new) in github
* `$ npm i sinopia2 -g`
* `$ npm i sinopia-github-oauth -g`

## Run
`$ sinopia`

## Configuration
Add the following in your `config.yaml`
```yaml
middlewares:
  github-oauth:
    client-id: github-app-id # required
    client-secret: github-app-secret # required

auth:
  github-oauth:
    org: soundtrackyourbrand # required, people within this org will be able to auth
    cache-ttl-ms: 60000 # default to 30s if not present
```

## Authenticating
You cannot use `npm login` to authenticate via this method, instead install [sinopia-github-oauth-cli](https://github.com/soundtrackyourbrand/sinopia-github-oauth-cli)
