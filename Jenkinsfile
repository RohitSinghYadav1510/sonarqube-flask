pipeline {
   agent none
    options {
        skipStagesAfterUnstable()
       }
  stages {
     
     stage('Test Application') {
            agent {
                docker {
                    image 'rohit1015/flasksonar:v3'
                   }
                }
            steps {
              sh 'py.test --cov-report xml:coverage.xml --cov=. --junitxml=result.xml test.py'
              }
        }
    }
}
