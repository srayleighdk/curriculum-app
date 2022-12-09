pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/srayleighdk/curriculum-app', branch: 'dev')
      }
    }

    stage('Log') {
      parallel {
        stage('Log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-End unit test') {
          steps {
            sh 'cd curriculum-front &&  npm i && npm i vue-jest &&  npm run test:unit'
          }
        }

      }
    }

  }
}