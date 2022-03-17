pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        echo 'this is the Compilation job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is the Testing job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the Packaging job'
        sh 'npm run package'
      }
    }

    stage('Archive') {
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
      echo 'This Pipeline has completed...'
    }

  }
}
