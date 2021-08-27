pipeline {
    agent any
    tools{
        maven 'local maven'
    }
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'start to save files'
                    archiveArtifacts artifacts: '**/target/*.war'

                }

            }
        }

    }
}
