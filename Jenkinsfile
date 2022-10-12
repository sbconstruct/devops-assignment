pipeline {
    agent {
        docker {
            image "maven:3.6.3-jdk-8"
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