pipeline {
  agent {
    label {
      label 'linux1'
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
        dir(path: '/tmp') {
          sh 'ls -latr'
        }
        
      }
    }
  }
}