pipeline {
  agent any
  stages {
    stage("build"){
      when {
        expression {
          env.BRANCH_NAME != 'dev'
        }
      }
      steps {
        echo 'building the aplication....'
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
