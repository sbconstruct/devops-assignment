pipeline {
    agent {
        docker {
            image "maven:3.8.6-jdk-8"
            label "docker"
        }
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