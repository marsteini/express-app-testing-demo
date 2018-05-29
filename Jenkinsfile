pipeline {
    agent { 
        docker { 
            image 'node:8'
            args "-u root:root"
        } 
    }
    stages {
        stage("Install packages...") {
            steps {
                sh "npm --version"
                sh "npm install"
            }
        }
        stage("Building app...") {
            steps {
                sh "npm build"
            }
        }
        stage("Building test...") {
            steps {
                sh "npm test"
                sh "npm run test:e2e"
            }
        }
    }
}