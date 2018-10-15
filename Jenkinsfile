
pipeline {
  agent 
     stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
 
     }
            post {
                failure { 
                    archive "target/**/*"
                    junit 'target/surefire-reports/*.xml'
                }
            }
      }
