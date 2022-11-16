node {
    stage('SCM') {
        checkout scm
    }
    stage('Example') {
        if (env.BRANCH_NAME == 'master') {
            echo 'I only execute on the master branch'
        } else {
            echo 'I execute elsewhere'
        }
    }
    post {
        success {
            discordSend webhookURL: 'https://discord.com/api/webhooks/1042290298262396938/lrenOCiI8f4UbarX5VJabW3yAZzqzJ8yFVbyw4ofz29cFJ3NLoVa_AKc1dM5v4OBWvx8'
        }
    }
}
