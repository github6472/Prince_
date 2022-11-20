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
        stage('Integration Testing')
            steps {
                sh 'mvn verify -DskipUnitTests'
            }
    }
}
