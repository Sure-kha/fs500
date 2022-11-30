
pipeline{
  agent any
  
  
  

  stages{
    
    stage("build node"){
      steps{
        script{
          echo "building the application..."
         
        }
        
  }
    
}
    stage("build image"){
      steps{
        script{
          echo "building the docker image..."
          sh 'docker build -t pipe.1.0 .'
        }
      }
    }
    
    stage("deploy"){
      steps{
        script{
          echo "deploying the application..."
        }
      }
     
    }
      }
    }


