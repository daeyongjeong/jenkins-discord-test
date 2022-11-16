pipeline {
    stage('Example') {
        if (env.BRANCH_NAME == 'main') {
            echo 'I only execute on the main branch'
            discordSend webhookURL: 'https://discord.com/api/webhooks/1042290298262396938/lrenOCiI8f4UbarX5VJabW3yAZzqzJ8yFVbyw4ofz29cFJ3NLoVa_AKc1dM5v4OBWvx8'
        } else {
            echo 'I execute elsewhere'
        }
    }
}
