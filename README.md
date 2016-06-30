# Launch Basic Example

[![Build Status](https://travis-ci.org/NewSpring/launch-basic-example.svg?branch=master)](https://travis-ci.org/NewSpring/launch-basic-example)

## launch.json

```json
{
  "ANDROID_BUILD_FOLDER": ".build/android",
  "ANDROID_STORE_PASS": "password",
  "ANDROID_KEY": "launch-basic-example",
  "ANDROID_ZIPALIGN": "path/to/zipalign",
  "ANDROID_HOCKEY_TOKEN": "token",
  "ANDROID_HOCKEY_ID": "id",
  "GALAXY_DEPLOY_HOSTNAME": "galaxy.meteor.com",
  "GALAXY_SESSION_FILE": "deployment_token.json"
}
```

## launch commands

```shell
$ launch galaxy launch-basic-example.meteorapp.com
$ launch build launch-basic-example.meteor.com
$ launch hockey
```

## Secrets

```
tar cvf secrets.tar launch.json .keystore deployment_token.json
travis encrypt-file secrets.tar .travis/secrets.tar.enc
```

