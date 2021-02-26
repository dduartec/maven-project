pipeline{
    /* A Declarative Pipeline */
    agent any

    stages{
        stage('Build'){
            steps{
                sh 'mvn clean package'
            }
            post{
                success{
                    echo 'Now Archiving'
                    archiveArtifact artifacts: '**/*.war'
                }                
            }
        }
    }
}