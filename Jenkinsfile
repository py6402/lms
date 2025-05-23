pipeline {
    agent any
    stages {
        stage('Code Analysis') {
            steps {
                echo 'CODE QUALITY CHECK'
                // Below command works in jenkins 
                sh 'cd webapp && sudo docker run --rm -e SONAR_HOST_URL="http://3.17.175.208:9000" -v ".:/usr/src" -e SONAR_TOKEN="sqp_64e4ddd0325ea51aa54516d2e8aa0af7c23a48c0" sonarsource/sonar-scanner-cli -Dsonar.projectKey=lms'
                echo 'CODE QUALITY COMPLETED'
            }
        }
        stage('Build Artifacts') {
            steps {
                echo 'Build LMS'
                sh 'cd webapp && npm install && npm run build'
                echo 'Build Completed'
            }
        }
        stage('Release Artifacts') {
            steps {
                sh 'cat /etc/os-release'
            }
        }
        stage('Deploy') {
            steps {
                sh 'ls'
            }
        }
        stage('Cleanup') {
            steps {
                sh 'ls'
            }
        }
    }
}
