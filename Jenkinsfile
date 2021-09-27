pipeline {
   agent {
     docker {
        image 'rohit1015/flasksonar:v2'
        }
     }
  stages {
     
     stage('Test Application') {
    
            steps {
              sh 'python test.py'
              }
        }
    }
}
