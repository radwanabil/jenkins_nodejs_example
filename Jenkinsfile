pipeline {
    agent any

    stages {
        stage('preparation') {
            steps {
            git 'https://github.com/radwanabil/jenkins_nodejs_example.git'
            }
}
        }
        
        
                stage('docker build') {
            steps {
withCredentials([usernamePassword(credentialsId: 'dockerhub', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                sh """

                docker build . -f dockerfile radwa98/sprints_jenkins_course:latest
                docker login -u ${USERNAME} -p ${PASSWORD}
                docker push radwa98/sprints_jenkins_course:latest
                """

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

        }
    }
}
