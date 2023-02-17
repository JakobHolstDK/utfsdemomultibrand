pipeline {
    agent any
    tools {
      jdk 'openjdk17'
      nodejs 'node16'
      groovy 'GROOVY3010'
    }
    options {
        disableConcurrentBuilds()
        buildDiscarder(logRotator(numToKeepStr: '10'))
    }

    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello world!"'
            }
        }
    }
}
