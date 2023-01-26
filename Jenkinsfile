pipeline {
  agent any
  stages {
    stage('test1') {
      parallel {
        stage('test1') {
          steps {
            sh 'echo "Bonjour le test windows"'
          }
        }

        stage('test2') {
          steps {
            sh '''echo "Pumpelup test linux"
'''
          }
        }

      }
    }

    stage('verifs') {
      steps {
        fileExists 'pom.xml'
        sh 'ls -la'
      }
    }

    stage('Build') {
      steps {
        sh 'mvn clean install'
      }
    }

    stage('report') {
      steps {
        echo 'PUBLISH'
      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }

  }
}