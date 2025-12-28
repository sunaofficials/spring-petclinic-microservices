pipeline {
    agent any

    environment {
        DOCKERHUB_USER = "sunaodisha"
        COMPOSE_FILE = "docker/docker-compose.yml"
    }

    stages {

        stage("Docker Login") {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'docker-gate',
                    usernameVariable: 'DOCKER_USER',
                    passwordVariable: 'DOCKER_PASS'
                )]) {
                    sh '''
                      echo "$DOCKER_PASS" | docker login -u "$DOCKER_USER" --password-stdin
                    '''
                }
            }
        }

        stage("Build Images") {
            steps {
                dir('spring-petclinic-microservices') {
                    sh 'docker-compose -f docker/docker-compose.yml build'
                }
            }
        }

        stage("Push Images") {
            steps {
                dir('spring-petclinic-microservices') {
                    sh 'docker-compose -f docker/docker-compose.yml push'
                }
            }
        }
    }

    post {
        success {
            echo "✅ All Petclinic images built and pushed successfully"
        }
        failure {
            echo "❌ Pipeline failed"
        }
    }
}
