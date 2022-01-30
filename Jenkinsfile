pipeline {
  agent any
  stages {
    stage('Start') {
      steps {
        sh 'echo "Something changed in repo"'
      }
    }

    stage('TEST is OK') {
      steps {
        sleep 5
      }
    }

    stage('Deploye') {
      parallel {
        stage('Deploy TESTserver') {
          steps {
            sh 'echo "Deployed!!!"'
          }
        }

        stage('Deploy Production') {
          steps {
            sh 'echo "Production deployed"'
          }
        }

      }
    }

    stage('Logging') {
      steps {
        sh 'echo "OK"'
      }
    }

  }
}