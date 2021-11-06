pipeline {
  agent any
  stages {
    stage('Start Process') {
      parallel {
        stage('Start Process') {
          steps {
            sh 'bash ${WORKSPACE}/main.sh'
          }
        }

        stage('Build Docker') {
          steps {
            sh 'git checkout develop'
          }
        }

        stage('Clone Repo') {
          steps {
            sh 'git checkout nuevaRama'
          }
        }

      }
    }

    stage('LaunchDocker') {
      steps {
        sh 'docker run -d -v /home/ubuntu/test:/home/test devos/devos'
      }
    }

    stage('Test') {
      steps {
        sh 'docker exec test run '
      }
    }

    stage('Deploy') {
      steps {
        echo 'Check'
      }
    }

  }
}