
pipeline {
  agent any
     stages {
        stage('Compile-Package') {
            steps {
              withMaven(maven : 'Maven 3.0.5') {
              sh 'mvn package'
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
