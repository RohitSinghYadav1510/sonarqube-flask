pipeline {
   agent {
     docker {
        image 'rohit1015/flasksonar:v3'
        }
     }
  stages {
     
     stage('Test Application') {
    
            steps {
              sh 'py.test --cov-report xml:coverage.xml --cov=. --junitxml=result.xml test.py'
              }
        }
    }
}
