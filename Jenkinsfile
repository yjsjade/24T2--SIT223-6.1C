post {
    always {
        emailext(
            subject: "Pipeline Notification ${BUILD_NUMBER}",
            to: 'jingshii.y@gmail.com',
            body: "This is a test email from Jenkins pipeline.",
            attachLog: true
        )
    }
}
