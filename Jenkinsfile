pipeline {
    agent {
        docker {
            image 'cypress/base:10'
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo "Running build ${env.BUILD_ID} on ${env.JENKINS_URL}"
                sh 'npm install dev'
                sh 'npm run test'
            }
        }
    }
}
