pipeline {
    agent any

    stages {
        stage('git checkout') {
            steps {
                git branch: 'master', url:'https://github.com/github6472/Prince_.git'
            }
        }
        stage('UNIT TESTING') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Integration TESTING') {
            steps {
                sh 'mvn verify -DskipUnitTests'
            }
        }
        stage('Maven Building') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
