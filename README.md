# KarmaHeadlessPoc

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.3.8. 
It's just a single POC to run tests with [Karma](https://karma-runner.github.io) using a Headless Browser (in this case, [ChromeHeadless](https://github.com/karma-runner/karma-chrome-launcher)) and Jenkins. 

CLI tests about the default app-component were used. 

## Running unit tests
Just run `npm test` to execute the unit tests. 
You must see 3 tests passing without any browser being opened.

## Running via Jenkins
Install and configure [NodeJS](https://wiki.jenkins.io/display/JENKINS/NodeJS+Plugin) plugin. 
