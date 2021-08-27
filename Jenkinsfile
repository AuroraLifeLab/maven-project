pipeline {
    agent any
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
