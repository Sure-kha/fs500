
pipeline{
  agent any
  tools{
    node 'nodejs'
  }
  
  

  stages{
    
    stage("build node"){
      steps{
        script{
          echo "building the application..."
          sh 'npm install'
        }
        
  }
    
}
    stage("build image"){
      steps{
        script{
          echo "building the docker image..."
          withCredentials([usernamePassword(credentialsId:'docker-hub',passwordVariable:'PASS',userVariable:'USER')])
          sh 'docker build -t surekha1988/demo-app:2.0 .'
          sh "echo $PASS | docker login -u $USER --password-stdin"
          sh 'docker push surekha1988/demo-app:2.0'
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


