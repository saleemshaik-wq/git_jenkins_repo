pipeline {
    agent { label 'slave1' }
    stages {
        stage('InstallMaven') {
            steps {
                sh "sudo apt update -y"
                sh "sudo apt install maven -y"
            }
        }
             stage('Checkout') {
              steps {
                sh "rm -rf git_jenkins_repo"
                sh "git clone https://github.com/saleemshaik-wq/git_jenkins_repo"
            }
        }
    }
}
