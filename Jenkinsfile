pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'mkdir -p Selenium'
                dir("Selenium")
                {
                    git branch: "main",
                    credentialsId: 'git',
                    url: 'https://github.com/amitkshatriya01/selenium.git'
                }
            }
        }
    }
}
