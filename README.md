# android-sdk-installer
Install Android SDK

[![Build Status](https://travis-ci.org/Commit451/android-sdk-installer.svg?branch=master)](https://travis-ci.org/Commit451/android-sdk-installer)
[![Gem](https://img.shields.io/gem/v/android-sdk-installer.svg)](https://rubygems.org/gems/android-sdk-installer)

## Setup
Install the gem:
```
gem install android-sdk-installer
```

## Usage
The installer looks for a `android-sdk-installer.yml` file in order to configure where the artifacts are and where they should go.
For example:
```yml
version: 25.2.3
platform: linux
components:
  - platform-tools
  - tools
  - build-tools-25.0.3
  - android-25
  - extra-google-m2repository
  - extra-android-m2repository

```
After creating this configuration, all you need to do is run:
```shell
android-sdk-installer
```

## Test Locally
Just run `ruby test/test.rb`. Set up your `android-sdk-installer.yml` as desired.

## Deployment
1. Adjust the version in the gemspec
2. `gem build dropbox-deployment.gemspec`
3. `gem push dropbox-deployment-version.number.here.gem`
4. Tag release in git

## Thanks
Thanks to the following for being a great reference on how to create a command line Ruby Gem:
  - http://robdodson.me/how-to-write-a-command-line-ruby-gem/

## License

android-sdk-installer is available under the MIT license. See the LICENSE file for more info.
