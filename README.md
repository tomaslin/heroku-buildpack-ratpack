Ratpack buildpack for heroku

This is a copy of the heroku buildpack components from ratpack foass https://github.com/danveloper/ratpack-foaas with a few alterations:

It detects that an applicatin is ratpack if it finds a file called src/ratpack/ratpack.groovy .

It doesn't automatically create a Procfile for running the application. Instead, you must specify a file called Procfile that contains your ratpack execution command. 

A sample Procfile for FOASS would look like this:

web: build/install/foaas/bin/foaas build/install/foaas/ratpack.groovy
