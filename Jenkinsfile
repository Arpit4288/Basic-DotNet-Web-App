pipeline {
    agent any

    environment {
        PATH = "/var/jenkins_home/tools/io.jenkins.plugins.dotnet.DotNetSDK/dotnetsdk/:$PATH"
    }

    stages {
        stage('Checkout') {
            steps {
                git(url: 'https://github.com/Arpit4288/Basic-DotNet-Web-App.git', branch: 'master')
            }
        }

        stage('Build') {
            steps {
                // Change directory to the location of your solution file
                dir('Basic DotNet Web App') {
                    // Execute the build command
                    sh 'dotnet build'
                }
            }
        }

        stage('Test') {
            steps {
                // Change directory to the location of your solution file
                dir('Basic DotNet Web App') {
                    // Execute the test command
                    sh 'dotnet test'
                }
            }
        }
    }
}
