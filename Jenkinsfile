pipeline {
    agent any

    stages {
        stage('preparation') {
            steps {
                // Get some code from a GitHub repository/
                git 'https://github.com/mahmoud254/jenkins_nodejs_example.git'
            }

         }
           stage('docker build') {
            steps {
                // Get some code from a GitHub repository/
                sh """
                   docker build . -f dockerfile -t mahmom/sprints_jenkins_course:latest
                   
                """
            }

         }
    }
}
