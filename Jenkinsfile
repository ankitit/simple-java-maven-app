
pipeline {
  agent any
     stages {
        stage('Build') {
            steps {
              withMaven(maven : 'Maven 3.0.5') {
              sh 'mvn clean package'
            }
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
