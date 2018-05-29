node("docker") {
    checkout scm
    stage("Installing packages...") {
        docker.image("node:8").inside {
            sh "npm --version"
            sh "npm install"
        }
    }
}