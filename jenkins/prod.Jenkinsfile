pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                bat 'mvn install'
            }
        }
        stage("Test") {
            steps {
                bat "mvn test"
            }
        }
        stage("CompiledandRunSonarAnalysis") {
            steps{
                bat 'mvn clean verify sonar:sonar -Dsonar.projectkey=hackdossier -Dsonar.organization=hackdossier -Dsonar.host.url=https://sonarcloud.io/ -Dsonar.token=ec9cdb38d5e716f14385f39185bd601de93c0ae1'
            }
        }
    }
}