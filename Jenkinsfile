pipeline {
    agent any

    tools {
        maven "3.8.6" 
    }
    stages {
        stage("Build") {
            steps {
                dir('my-app') {
                sh "mvn -version"
                sh "mvn clean install"
                }

            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}