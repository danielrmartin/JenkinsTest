#! groovy
pipeline {
  agent {
    node {
      label 'docker'
    }
    
  }
  stages {
    stage('foo') {
      steps {
        sh 'echo hello'
        bar(foo,bar)
        
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh 'echo This is a test'
          }
        }
        stage('test2') {
          steps {
            sh 'echo test more stuff'
          }
        }
      }
    }
    stage('deploy to dev') {
      steps {
        dir(path: 'Danny') {
          sh 'ls -latr'
        }
        
      }
    }
    stage('post') {
      steps {
        catchError() {
          echo 'WOrd'
        }
        
      }
    }
  }
}
