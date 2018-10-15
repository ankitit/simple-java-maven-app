try{
       
  node{
    
    stage('Git Checkout'){
      
      git 'https://github.com/ankitit/simple-java-maven-app.git'
      
    }
     
    stage('Maven Build'){
       
        sh 'mvn clean package'
      
    }
    
    
    
    }  
    }catch(error) {
      currentBulid.result = 'FAILURE'
      throw error
    }
   
  
