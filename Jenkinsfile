pipeline {
    agent any
    tools{
        maven 'maven3.8.8'
    }

    stages {
        stage('Checkoput SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/JesfrinGnZ/devops-practice.git'
            }
        }
        stage('Build'){
            steps {
                sh 'mvn clean package -Dskiptests -B -ntp'
            }
        }
    }
}