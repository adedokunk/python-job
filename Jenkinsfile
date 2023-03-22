pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
      }
    }
    stage('hello') {
      steps {
        sh 'python3 check_endpoint.py'
      }
    }
    stage('build') {
      steps {
        echo "test"
      }
    }  
    stage ('Create zip') {
            steps {
                sh 'zip middlewareScript-${BUILD_NUMBER}.zip * --exclude Jenkinsfile README.md'
                
            }
        }
  }
  }

