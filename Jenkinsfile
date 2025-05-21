pipeline {
    agent any

    // environment {
    //     DOCKER_CREDENTIAL_ID = 'e36e7080-5f61-4d38-bc9a-ff0576cacb5e'  // Replace with your actual Jenkins credential ID
    // }

    stages {
        stage ("Login to Docker") {
            steps {
               // withCredentials([string(credentialsId: DOCKER_CREDENTIAL_ID, variable: 'DOCKER_TOKEN')]) {
                  //  sh 'echo $DOCKER_TOKEN | docker login --username minfyakhilesh --password-stdin'
                docker login -u minfyakhilesh -p Akhilesh@123
                }
            }
        }
        stage ("Build Image") {
            steps {
                sh 'docker build -t minfyakhilesh/app1 .'
            }
        }
        stage ("Push Image") {
            steps {
                sh 'docker push minfyakhilesh/app1'
            }
        }
    }
}

