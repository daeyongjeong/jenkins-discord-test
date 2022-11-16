pipeline {
    agent {
        node {
            label 'labelName'
        }
    }
    stages {
        stage('SCM') {
            steps {
                checkout scm
            }
        }
        stage('Example') {
            steps {
                script {
                    if (env.BRANCH_NAME == '*/main') {
                        echo 'I only execute on the main branch'
                    } else {
                        echo 'I execute elsewhere'
                    }
                }
            }
        }
    }
    post {
        always {
            discordSend webhookURL: 'https://discord.com/api/webhooks/1042290298262396938/lrenOCiI8f4UbarX5VJabW3yAZzqzJ8yFVbyw4ofz29cFJ3NLoVa_AKc1dM5v4OBWvx8'
        }
    }
}
