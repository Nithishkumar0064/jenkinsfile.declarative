pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/artisantek/java-example.git'
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
                sh 'sudo cp /home/ubuntu/new-folder/workspace/assignment-declarative/target/*.war  /opt/tomcat/apache-tomcat-9.0.68/webapps/'
            }
        }

    }

}
