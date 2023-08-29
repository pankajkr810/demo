pipeline {
    agent any
    
    stages {
        // Your build stages here
    }
    
    post {
        success {
            emailext subject: "Build Successful",
                      body: "The build was successful. Here's the attached file.",
                      to: 'recipient@example.com',
                      attachmentsPattern: 'dir/**/*.txt'
        }
    }
}
