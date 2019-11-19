pipeline {
    agent {
        docker { image 'node:7-alpine' }
    }

    stages {
      stage('Setup') {
        steps {
          script {
                def json = readJSON file:'myTest.json'
                echo "name: Dayantha"
                writeFile(file:'myTest.json', text: json)
          
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
