def gv
pipeline{
  agent any
  parameters{
    choice(name:'VERSION',choices:['1.1.0','1.2.0','1.3.0'],description:'')
    booleanParam(name:'excuteTests',defaultValue:true,description:'')
  }

  stages{
    stage("init"){
      steps{
        script{
          gv=load "script.groovy"
        }
      }
    }
    stage("build"){
      steps{
        script{
          gv.buildApp()
        }
        
  }
    
}
    stage("test"){
      when{
        expression{
          params.excuteTests
        }
      }
      steps{
        echo 'testing the application...'
      }
    }
    stage("deploy"){
     
      steps{
         echo 'deploying the application...'
        echo "deploying version ${params.VERSION}"
      }
    }
      }
    }


