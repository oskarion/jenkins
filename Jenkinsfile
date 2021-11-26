pipeline {
  agent any
  
  environment {
    NEW_VERSION = '1.1.0'
  }  
  
  parameters {
    booleanParam(name: 'executeTests', defaultValue: true, description:'')
  }

  stages {
    stage("build"){
      when {
        expression {
          env.BRANCH_NAME == 'dev' || env.BRANCH_NAME == 'bug_fix'
        }
      }
      steps {
        echo 'building the aplication....'
        echo "building version ${env.NEW_VERSION}"
      }
      
    }
    stage("test"){
      when {
        expression {
          params.executeTests == true
        }
      }
      steps {
        echo 'testing the aplication...'
        echo "executeTests variable = {$params.executeTests}"
      }
      
    }
    stage("deploy"){
      steps {
        echo 'deployin the aplication...'
      }
      
    }

  }
}
