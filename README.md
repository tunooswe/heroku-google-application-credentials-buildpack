# heroku-google-application-credentials-buildpack
Generates a Google credential file based on Heroku Config Vars.

This is useful when using a package such as [@google-cloud/storage](https://www.npmjs.com/package/@google-cloud/storage) which loads credentials from a file instead of an environmental variable.

This repository is a fork from [elishaterada/heroku-google-application-credentials-buildpack](https://github.com/elishaterada/heroku-google-application-credentials-buildpack). It fixes some bugs that I found during my usage of the original repository.

## Usage

1. Create Config Vars key `GOOGLE_CREDENTIALS` and paste the content of service account credential JSON file as is.
2.  Create a key under Config Vars `GOOGLE_APPLICATION_CREDENTIALS` and set a value as `google-credentials.json`.

The script with generate a file called `google-credentials.json` which holds the key from the step #1 above.
