pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        sh 'echo "test"'
      }
    }

    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'succesfull'
          }
        }

        stage('rest') {
          steps {
            echo 'parallel job'
            echo 'parallel2 job'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        sleep 15
      }
    }

  }
}