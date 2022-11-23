pipeline {
  agent any
  stages {
    stage('build-the-app') {
      steps {
        echo 'this is the first job'
        sh 'npm install'
      }
    }

    stage('test-the-app') {
      steps {
        echo 'this is the second job'
        sh 'npm test'
      }
    }

    stage('package-the-app') {
      steps {
        echo 'this is the third job'
        sh 'npm run package'
      }
    }

    stage('archive-artifacts') {
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
      echo 'this is my first pipeline as code...'
    }

  }
}