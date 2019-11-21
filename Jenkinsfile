pipeline {
            agent {
                docker { image 'node:12-alpine' }
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
      stage('Artifacts') {   
            steps {
                copyArtifacts projectName: 'YAML Test', selector: specific('')
            }
        }         
      }

    post {
      success {
        echo 'Completed'
      }
    }
}
