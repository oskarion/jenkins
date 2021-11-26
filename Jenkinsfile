pipeline {
  agent any
  environment {
    NEW_VERSION = '1.1.0'
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
        echo "building version ${NEW_VERSION}"
      }
      
    }
    stage("test"){
      steps {
        echo 'testing the aplication...'
      }
      
    }
    stage("deploy"){
      steps {
        echo 'deployin the aplication...'
      }
      
    }

  }
}
