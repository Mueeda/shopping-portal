pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'This is the build job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'This is the test job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'This is the package job'
        sh 'npm run package'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'This is my first pipeline as code !'
    }

  }
}