pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git(url: 'https://github.com/Arpit4288/Basic-DotNet-Web-App.git', branch: 'master')
            }
        }

        stage('Build') {
            steps {
                bat 'dotnet build'
            }
        }

        stage('Test') {
            steps {
                bat 'dotnet test'
            }
        }
    }
}
