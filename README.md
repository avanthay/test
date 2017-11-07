### Testing

* To run unit tests use either `meteor yarn run test`, `meteor yarn run test-browser` or `meteor yarn run test-debug` (see the repo's [README](https://gitlab.inf.ethz.ch/OU-LECTURERS/code_expert/blob/master/README.md) for details about running unit tests and configuring the IDE)
* To write unit tests (and you should! :smirk:)
  * First create a file with the same name as the one to be tested and add `.test` or `.tests` before the file ending (e.g. if you want to write tests for `Loading.jsx`, create a blank file and name it `Loading.test.jsx`)
  * Add `/* eslint-env mocha */` at the top of the file, to prevent ESLint to report non existing issues
  * You also may add `/* eslint-disable no-unused-expressions */` if you make use of chai expressions
  * Write your unit tests into your newly created file referring to the [meteor guide](https://guide.meteor.com/testing.html#unit-testing)
    * Make use of the following libraries as recommended by meteor
      * [Mocha](https://mochajs.org/) as test runner
      * [Chai](http://chaijs.com/) for assertions
      * [Factory](https://github.com/versolearning/meteor-factory) to generate data
      * [Faker](https://github.com/Marak/Faker.js) to generate random data content
      * [Sinon](http://sinonjs.org/) to stub stuff and [StubCollection](https://github.com/hwillson/meteor-stub-collections) to mock the database
    * Unfortunatly, WebStorm does not resolve meteor atmosphere dependencies, so you won't get autocompletion and linked documentation while writing your tests. Therefore please refer to the respective documentation available on the links above. Moreover vote for the [WebStorm issue WEB-21682](https://youtrack.jetbrains.com/issue/WEB-21682) at JetBrains to stay informed as soon as a fix is available.
* As a reference, the following example unit tests are implemented:
  * `Loading.tests.jsx` as React unit test sample with the usage of [Enzyme's shallow](https://github.com/airbnb/enzyme/blob/master/docs/api/shallow.md) and [Chai's expect](http://chaijs.com/api/bdd/)
  * `EnvReader.tests.js` as sample for testing a plain JS class
  * `Exercises.tests.js` as Collection unit test sample with [Faker](http://marak.github.io/faker.js/#toc6__anchor) and [Sinon's stubs](http://sinonjs.org/releases/v3.2.0/stubs/)
* Integration tests are not implemented for now, if you want to make use of it please refer to the [documentation of meteor](https://guide.meteor.com/testing.html#integration-testing) and append `-- --full-app` to the test command to run it
