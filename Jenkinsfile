#! groovy
  node () {
    stage('foo') {
        sh 'echo hello'
    }
    stage('Test') {
            sh 'echo test more stuff'
    }
    stage('deploy to dev') {
  
        dir(path: 'Danny') {
          sh 'ls -latr'   
        }
       // deploy('QA')
      
    }
    stage('post') {
      
        catchError() {
          echo 'Word'
        }
    }
  }
