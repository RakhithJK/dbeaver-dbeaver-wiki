DBeaver uses tycho-surefire to run JUnit tests in OSGi environment. This fact may complicate a bit the process of writing and running unit tests for DBeaver. Let's take a look at possible ways to do that.

### Using UNIX shell

Suppose we introduced some changes to our code and want to run the tests. It's actually quite easy:

```
$ cd /path/to/project/
$ mvn clean install 
```
This compiles the project and runs unit tests.

If we want to only run unit tests:

```
$ cd test
$ mvn clean verify
```

Unit tests are separated into bundles. If you want to only run tests only from a specific bundle, navigate to that bundle and run `mvn clean verify` there.

It's also worth pointing out that you need to recompile the whole project with `mvn clean install` after every change in the project's codebase before running unit tests, otherwise, you will be running tests against the previous version and it may lead to all sorts of confusion. 