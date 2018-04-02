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
        bar(env.GIT_URL,env.BRANCH_NAME)
        
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
        deploy('QA')
      }
    }
    stage('post') {
      steps {
        catchError() {
          echo 'Word'
        }
        
      }
    }
  }
}
