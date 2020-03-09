# Weekend

## Packages and Modules

* node_modules should be .gitignored and not committed to your project's git repo

* Library: an independent collection of code that can be used by programs (not JS specific)
* Module: JS code in a separate file, that can be required by other JS programs * Package: a collection of JS modules, with a package.json, usually published on NPM

* require() imports functionality or data from another module

* Dependencies are installed in ./node_modules 

## Automated Testing

* Unit Testing -> small pieces of code; individual functions; isolated
  * Mocha, Jasmine, Tape

* Integration Testing -> how parts of system work together
  * When unit testing alone is not enough

* Functional Testing (AKA Browser/E2E Testing) -> tests complete functionality of the application
  * Selenium


* Behaviour Driven Development
  * Specify behaviour based on user stories that are broken down into scenarios that can be built and tested

## Mocha and Chai

*  Make directory called test/ in project's root directory for testing code
* To test in Node.js, add `var chai = require('chai');`

* `describe` is used to group individual tests
* `it` is used to describe the actual tests

* `npm install mocha chai --save-dev'
  * `--save-dev` package will appear in your devDependencies
  * Means that they are modules that are only required during development