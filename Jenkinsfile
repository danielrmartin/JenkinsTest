pipeline {
  agent {
    node {
      label 'maven-jdk-8'
    }
    
  }
  stages {
    stage('foo') {
      steps {
        sh 'echo hello'
      }
    }
    stage('Test') {
      steps {
        parallel(
          "Test": {
            sh 'echo This is a test'
            
          },
          "test2": {
            sh 'echo test more stuff'
            
          }
        )
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