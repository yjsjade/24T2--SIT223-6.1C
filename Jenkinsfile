pipeline {
    agent any
    stages {
        stage('Send Email') {
            steps {
                script {
                    emailext(
                        subject: "Test Email ${env.BUILD_NUMBER}",
                        to: 'jingshii.y@gmail.com',
                        mimeType: 'text/html',
                        body: "This is a test email sent from Jenkins.",
                        attachLog: true
                    )
                }
            }
        }
    }
}
