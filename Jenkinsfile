
pipeline{
  agent any
  
   stages{
    
    stage("test"){
      steps{
        script{
        echo 'testing the application.....'
        echo "Excuting the application for branch $BRANCH_NAME"
        }
  }
    
}
    stage("build image"){
      when {
        expression{
          BRANCH_NAME =='main'
        }
      }
      steps{
        script{
          echo "Building the application..."
        }
        
      }
    }
    
    stage("deploy"){
       when {
        expression{
          BRANCH_NAME =='main'
        }
      }
      steps{
        script{
          echo "deploying the application..."
        }
      }
     
    }
      }
    }


