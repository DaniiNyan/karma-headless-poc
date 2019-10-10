#!/usr/bin/env groovy

node {
  env.NODEJS_HOME = "${tool 'Node 12.8.0'}"
  env.PATH = "${env.NODEJS_HOME}/bin:${env.PATH}:/usr/local/bin"
  sh "echo $DISPLAY"

  stage('Checkout') {
    checkout scm
  }  

  stage('Install dependencies') {
    print "Install dependencies"
    sh "npm install"
  }

  wrap([$class: 'Xvfb']) {
    stage('Unit tests') {
      print "Running unit tests"
      sh "echo $DISPLAY"
      sh "npm test"
    }
  }

  stage('Show success message') {
    print "Succes!"
  }
}
