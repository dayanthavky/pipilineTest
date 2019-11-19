pipeline {
    agent {
        docker { image 'node:7-alpine' }
    }

    stages {
      stage('Setup') {
        steps {
          script {
                def data = readJSON file:'myTest.json'
                echo "name: Dayantha"
          
            }
          }
        }
      }

    post {
      success {
        echo 'Completed'
      }
    }
}
