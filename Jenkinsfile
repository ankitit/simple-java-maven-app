try{
       
  node{
    
    stage('Git Checkout'){
      
      git 'https://github.com/ankitit/simple-java-maven-app.git'
      
    }
     
    stage('Maven Build'){
       
        sh 'clean package'
      
    }
    
    
    
    }  
    }catch(error) {
      currentBulid.result = 'this is fucked up'
      throw error
    }
   
  
