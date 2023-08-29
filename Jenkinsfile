pipeline {
    agent any
    
    stages {
        stage('merge-jar-output')
           {
            steps {
                sh '''
                pwd
                ls
            }
           }
    }
    
    post {
    success {
      sh'''
      pwd
      ls
      '''
      emailext (
        subject: "Build Successful",
                      body: "The build was successful. Here's the attached file.",
                      to: 'anshika.tiwari@robomq.io',
                      attachmentsPattern: 'dir/**/*.txt'
        )
    }
    }
}
