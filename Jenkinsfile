pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000 -p 5000:5000'
            echo 'Node image in Docker is completed.'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Start installing npm.'
                sh 'npm install'
                
            }
        }
        stage('Test') {
            steps {
                echo 'Executing test shell script.'
                sh './jenkins/scripts/test.sh'
            }
            
        }
    }
}
