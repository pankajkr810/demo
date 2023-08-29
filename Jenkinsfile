pipeline {
    agent any
    
    stages {
        stage {
            steps {
                echo "hello"
        }
    }
    
    post {
        success {
            emailext subject: "Build Successful",
                      body: "The build was successful. Here's the attached file.",
                      to: 'anshika.tiwari@robomq.io',
                      attachmentsPattern: 'dir/**/*.txt'
        }
    }
}
