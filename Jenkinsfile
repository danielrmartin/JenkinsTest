#! groovy
  node () {
    stage('foo') {
        sh 'echo hello;env'
      //  bar(env.GIT_URL,env.BRANCH_NAME)
    }
    stage('Test') {
            sh 'echo test more stuff for sure'
    }
    stage('deploy to dev') {
  
        dir(path: 'Danny') {
          sh 'ls -latr'   
        }
     //   deploy('QA')
      
    }
    stage('post') {
      
        catchError() {
          echo 'Word'
        }
    }
  }
