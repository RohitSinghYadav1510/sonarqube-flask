pipeline {
   agent {
     docker {
        image 'rohit1015/flasksonar:v1'
        }
     }
  stages {
     
     stage('Test Application') {
    
            steps {
              sh 'python test.py --cov-report xml:coverage.xml --cov=. --junitxml=result.xml'
              }
        }
    }
}
