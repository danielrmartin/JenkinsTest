#! groovy
  node () {
    stage('foo') {
        sh 'echo hello2'
    }
    stage('Test') {

            sh 'echo test more stuff for sure'
    }
    stage('deploy to dev') {
  
        dir(path: 'Danny') {
          sh 'env'   
        }

       // deploy('QA')

      
    }
    stage('post') {
      
        catchError() {
          echo 'Word'
        }
    }
  }
