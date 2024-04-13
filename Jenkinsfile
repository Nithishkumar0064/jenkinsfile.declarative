pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Nithishkumar0064/java-example.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Push') {
            steps {
                echo 'This is Push Stage'
            }
        }

        stage('Deploy') {
            steps {
                sh 'sudo cp /home/ubuntu/jenkins/workspace/jenkinsfile.declarative/target/*.war  /opt/tomcat/apache-tomcat-9.0.68/webapps/'
            }
        }

    }

}
