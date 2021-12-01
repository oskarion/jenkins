pipeline {
  agent any
  
  environment {
    NEW_VERSION = '1.1.0'
    NEW_ENV = 'new_env_value'
  }  
  
  parameters {
    booleanParam(name: 'executeTests', defaultValue: true, description:'')
    string(name: 'string_check', defaultValue: 'checked', description:'')
  }

  stages {
    stage("build"){
      when {
        expression {
          env.BRANCH_NAME == 'bug_fix'
        }
      }
      steps {
        echo 'building the aplication....'
        echo "value of NEW_ENV environemntal variable is ${env.NEW_ENV}"
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
        echo "executeTests variable = ${params.executeTests}"
      }
      
    }
    stage("deploy"){
        when {
          expression {
           environment(name: "NEW_VERSION", value: "1.1.0") && params.string_check == 'checked'
          }
        }
      steps {
        echo 'deployin the aplication...'
      }
      
    }

  }
}
