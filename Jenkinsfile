pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git 'https://github.com/narendrasingamaneni91/example-ruby-app.git'
      }
    }
    stage('build') {
      parallel {
        stage('build') {
          steps {
            sh 'mvn install'
          }
        }
        stage('qa-build') {
          steps {
            sh 'mvn package'
          }
        }
      }
    }
    stage('deploy') {
      steps {
        sh '#!/bin/bash'
      }
    }
  }
}