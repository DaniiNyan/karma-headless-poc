#!/usr/bin/env groovy

node {

    env.NODEJS_HOME = "${tool 'Node 12.8.0'}"
    env.PATH = "${env.NODEJS_HOME}/bin:${env.PATH}:/usr/local/bin"

    stage('Checkout') {
      checkout scm
    }

    stage('Install dependencies') {
      print "Install dependencies"
      sh "npm install"
    }

    stage('Unit tests') {
     print "Running unit tests"
     sh "npm"
    }

    stage('Show success message') {
      print "Succes!"
    }

  } catch (caughtError) {
    currentBuild.result = "FAILURE"
    throw caughtError
  }

}
