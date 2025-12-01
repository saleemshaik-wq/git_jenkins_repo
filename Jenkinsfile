pipeline {
  // agent { label 'Java' }
     agent none
      parameters {
string(name: 'cmd', defaultValue: 'default', description: 'A sample string parameter')
booleanParam(name: 'SAMPLE_BOOLEAN', defaultValue: true, description: 'A boolean parameter')
choice(name: 'cmd1', choices: ['install', 'compile'], description: 'Choose one option')
}
    stages {
             stage('Checkout') {
                 agent { label 'Java' }
              steps {
                sh "rm -rf git_jenkins_repo"
                sh "git clone https://github.com/saleemshaik-wq/git_jenkins_repo"
            }
        }
    }
}
