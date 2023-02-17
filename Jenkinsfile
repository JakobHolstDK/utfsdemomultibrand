pipeline {
    agent any
    tools {
      gradle 'gradle8'
    }
    stages {
        stage('Unit test') {
          steps {
              script {
                  sh 'echo "Udfører statisk kodeanalyse og unit tests..."'
                  sh './gradlew clean check --no-build-cache'
              }
          }
          post {
              always {
                  junit keepLongStdio: true, testResults: '**/**/build/test-results/test/*.xml'
              }
          }
        }

        stage('Build') {
            steps {
                sh 'echo "Hello world!"'
            }
        }
    }
}
