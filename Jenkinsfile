pipeline {
   agent {
     docker {
        image 'rohit1015/flasksonar:v1'
        }
     }
  stages {
     
     stage('Test Application') {
    
            steps {
              sh 'python py.test --cov-report xml:coverage.xml --cov=. --junitxml=result.xml'
              sh 'python test.py'
              }
        }
    }
}
