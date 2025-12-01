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
                withCredentials([
                    usernamePassword(
                        credentialsId: '2424c737-2500-4d14-a0e3-81e8577205c4',
                        usernameVariable: 'Shaik_USER',
                        passwordVariable: 'Shaik_PASS'
                    )
                    /*
                    sshUserPrivateKey(
                        credentialsId: '6de0e10a-7954-47f8-9c09-a6bf341a387f',
                        keyFileVariable: 'Shaik_SSH_KEY',
                        usernameVariable: 'Shaik_SSH_USER'
                    )
                    */
                ]) {
                    sh "rm -rf git_jenkins_repo"
                    sh "git clone https://github.com/saleemshaik-wq/git_jenkins_repo"
                }
            }
        }
    }
}
