pipeline {
            agent {
                docker { image 'maven:3-alpine' }
            }

    stages {
      stage('Setup') {
        steps {
          script {
                def json = readJSON file:'myTest.json'
                jsonFile = json.get(0);
                jsonFile['name'] = "Dayantha"
                echo "${json}"
          
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
