#! groovy
  node () {
    stage('foo') {
        sh 'echo hello2'
    }
    stage('Test') {
            sh 'echo test more stuff and junk'
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
