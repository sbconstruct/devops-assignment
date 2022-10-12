pipeline {
    agent any

    tools {
        maven "3.6.0" // You need to add a maven with name "3.6.0" in the Global Tools Configuration page
    }
    

    // agent {
    //     docker {
    //         image "maven:3.6.3-jdk-8"
    //         label "docker"
    //     }
    // }
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