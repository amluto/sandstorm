# Sandstorm Tests

## Setup

First, you need to install Java in order to run Selenium. Under Debain/Ubuntu, this can be accomplished with `sudo apt-get install default-jre-headless`.

Second, from the tests directory, run `npm install` to install all the node dependencies.

Third, firefox must be installed on the system.

## Run Tests

First, you have to be running selenium server. You can start one with `./node_modules/selenium-standalone/bin/start-selenium`. Wait for a line that looks like `Started org.openqa.jetty.jetty.Server...` before running tests. If you are running on a headless system, you will need to run `xvfb` in order to allow firefox to be runnable by selenium. You can do this by running `sudo Xvfb :10 -ac`, and then `export DISPLAY=:10` before starting selenium.

Run the tests with `npm test`. This requires a running instance of sandstorm, and **WILL** potentially change the database. If you aren't comfortable with that, run with `./run-docker.sh`. If running with docker, you will want to run `make .docker` in the parent directory first. Also, make sure you have a relatively recent version of Docker installed (v1.1+).
```
