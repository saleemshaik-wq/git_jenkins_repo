pipeline {
    agent { label 'Java' }
    stages {
             stage('Checkout') {
              steps {
                sh "rm -rf git_jenkins_repo"
                sh "git clone https://github.com/saleemshaik-wq/git_jenkins_repo"
            }
        }
    }
}
