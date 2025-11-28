pipeline {
  // agent { label 'Java' }
     agent none
    stages {
             stage('Checkout') {
                 agent { label 'Java' }
              steps {
                sh "rm -rf git_jenkins_repo"
                sh "git clone https://github.com/saleemshaik-wq/git_jenkins_repo"
            }
        }
        stage('Checkout') {
                 agent { label 'Java' }
              steps {
                  sh "mvn clean package"
    }
}
