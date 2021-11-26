pipeline {
  agent any
  stages {
    stage("build"){
      when {
        expression {
          env.BRANCH_NAME != 'dev' && env.BRANCH_NAME != 'bug_fix'
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
