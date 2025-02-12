pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/gurumurthy974/day2session.git'  // Replace with your actual repo URL
            }
        }
        stage('Build with Maven') {
            steps {
                sh 'mvn clean package'  // Builds the JAR/WAR file
            }
        }
        stage('Deploy with Ansible') {
            steps {
                sh 'ansible-playbook -i inventory.ini deploy.yml'  // Calls Ansible for deployment
            }
        }
    }
}
