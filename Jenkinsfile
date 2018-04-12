#! groovy
  node () {
    stage('foo') {
        sh 'echo hello'
        bar(env.GIT_URL,env.BRANCH_NAME)
    }
    stage('Test') {
      parallel {
        stage('Test') {
            sh 'echo This is a test'
        }
        stage('test2') {
          
            sh 'echo test more stuff'
        }
      }
    }
    stage('deploy to dev') {
  
        dir(path: 'Danny') {
          sh 'ls -latr'   
        }
        deploy('QA')
      
    }
    stage('post') {
      
        catchError() {
          echo 'Word'
        }
    }
  }
