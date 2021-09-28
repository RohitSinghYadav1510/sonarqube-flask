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
    
     stage("Code Analysis"){
          agent any
          steps {
            sh 'docker run --rm --net=host -v pwd:/sonarqube-flask sonarsource/sonar-scanner-cli sonar-scanner -Dsonar.projectKey=sonarqube-flask -Dsonar.projectBaseDir=/sonarqube-flask -Dsonar.host.url=http://35.154.184.115:9000 -Dsonar.login=1accaab945bf018af4d31668e92d30e7d46551d7'
            }
      
         }
    }
}
