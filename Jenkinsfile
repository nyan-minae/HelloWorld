pipeline {
  agent {
    dockerfile {
      filename 'dockerfile'
    }

  }
  stages {
    stage('Npm Build') {
      steps {
        sh 'npm install && npm run build'
      }
    }
  }
  post {
    success {
      echo 'I succeeeded!'

    }

    unstable {
      echo 'I am unstable :/'

    }

    failure {
      echo 'I failed :('

    }

  }
  triggers {
    pollSCM('H/2 * * * *')
  }
}