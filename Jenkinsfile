pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    def branch = env.BRANCH_NAME ?: 'main'
                    sshagent(['id_github_jenkins']) {
                        sh "git clone -b ${branch} git@github.com:ums-messaging/ums.git"
                    }
                }
            }
        }
    }
}
