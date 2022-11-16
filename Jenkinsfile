pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'hello world'
            }
        }
    }
    post {
            success {
                discordSend description: '알림테스트',
                  footer: '테스트 빌드가 성공했습니다.',
                  link: env.BUILD_URL, result: currentBuild.currentResult,
                  title: '테스트 젠킨스 job',
                  webhookURL: '{webhook주소}'
            }
            failure {
                discordSend description: '알림테스트',
                  footer: '테스트 빌드가 실패했습니다.',
                  link: env.BUILD_URL, result: currentBuild.currentResult,
                  title: '테스트 젠킨스 job',
                  webhookURL: '{webhook주소}'
            }
    }
}
