
pipeline {
  agent any
     stages {
        stage('Compile-Package') {
            steps {
              withMaven(maven : 'maven 3.0.5') {
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
  }
