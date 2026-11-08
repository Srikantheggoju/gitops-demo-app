pipeline {
    agent any

    environment {
        IMAGE = "srikantheggoju/gitops-demo"
    }

    stages {

        stage('Build Image') {
            steps {
                sh 'docker build -t $IMAGE:$BUILD_NUMBER .'
            }
        }

        stage('Push Image') {
            steps {
                sh 'docker push $IMAGE:$BUILD_NUMBER'
            }
        }
    }
}
