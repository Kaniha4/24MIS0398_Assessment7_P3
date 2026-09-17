pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'YOUR_GITHUB_REPOSITORY_URL'
            }
        }

        stage('Parallel Checks') {
            parallel {
                stage('Student Data Check') {
                    steps {
                        echo 'Checking student information...'
                        bat 'javac StudentManagement.java'
                    }
                }

                stage('Academic Performance Check') {
                    steps {
                        echo 'Checking academic performance system...'
                        bat 'java -version'
                    }
                }
            }
        }
    }
}
