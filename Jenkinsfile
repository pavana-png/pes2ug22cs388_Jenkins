pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output YOUR_SRN-1.cpp'
                }
            }
        }

       stage('Test') {
    steps {
        script {
            sh './wrong_binary' // Intentional error
        }
    }
}


        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed ❌'
        }
    }
}
