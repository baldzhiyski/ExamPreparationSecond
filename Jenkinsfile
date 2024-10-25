pipeline {
    agent any
    when {
        branch 'feature-ci-pipeline'
    } 
    stages {
        stage('Restore dependencies') { 
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Dotnet Build') { 
            steps {
              bat 'dotnet build --no-restore'
            }
        }
        stage('Execute Tests') { 
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
