pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        sh 'composer install --no-interaction'
      }
    }

    stage('Test') {
      steps {
        sh './vendor/bin/phpunit'
      }
    }

  }
}