pipeline {
    agent {
        docker {
            image 'cypress/base:10'
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
