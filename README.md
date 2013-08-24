#travis-ci saucelabs template

[![Build Status](https://travis-ci.org/cioddi/travis-ci-saucelabs-template.png)](https://travis-ci.org/cioddi/travis-ci-saucelabs-template)

simple template for functional php tests using travis-ci and saucelabs


##Saucelabs username and access token

Encrypt username and access token using the travis gem

```
travis encrypt SAUCE_USERNAME={SAUCELABS_USERNAME} -r {GITHUB_USERNAME}/{GITHUB_REPOSITORY_NAME}
travis encrypt SAUCE_ACCESS_KEY={SAUCE_ACCESS_TOKEN} -r {GITHUB_USERNAME}/{GITHUB_REPOSITORY_NAME}
```

and insert the encrypted values into your .travis.yml

```
env:
  global:
    - secure: {ENCRYPTED_USERNAME}
    - secure: {ENCRYPTED_ACCESS_TOKEN}
```

You will be able to access them within the travis test server as environment variables (SAUCE_USERNAME, SAUCE_ACCESS_KEY)

##MIT license
Copyright (c) 2013 Max Tobias Weber