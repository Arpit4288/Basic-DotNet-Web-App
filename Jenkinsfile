pipeline {
    agent any

    // Define the environment variables for the .NET SDK
    environment {
        DOTNET_SDK = '.NET6' // Name of the .NET SDK defined in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git(url: 'https://github.com/Arpit4288/Basic-DotNet-Web-App.git', branch: 'master')
            }
        }

        stage('Build') {
            // Use the build wrapper to set up the environment with the specified .NET SDK
            wrappers {
                dotnetSdkInstallation("$DOTNET_SDK") // Specify the .NET SDK to use
            }
            steps {
                // Change directory to the location of your solution file
                dir('Basic DotNet Web App') {
                    // Execute the build command using shell
                    sh 'dotnet build'
                }
            }
        }

        stage('Test') {
            // Use the build wrapper to set up the environment with the specified .NET SDK
            wrappers {
                dotnetSdkInstallation("$DOTNET_SDK") // Specify the .NET SDK to use
            }
            steps {
                // Change directory to the location of your solution file
                dir('Basic DotNet Web App') {
                    // Execute the test command using shell
                    sh 'dotnet test'
                }
            }
        }
    }
}
