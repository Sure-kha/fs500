
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
          withCredentials([usernamePassword(credentialsId: 'docker-hub', passwordVariable: 'dockerHubPassword', usernameVariable: 'dockerHubUser')]) {
        	sh "docker login -u ${env.dockerHubUser} -p ${env.dockerHubPassword}"
          sh 'docker push surekha1988/pipeline:2.0'
          }
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


