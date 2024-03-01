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
                // echo 'Testing..'
                // sh 'mkdir -p Selenium'
                // dir("Selenium")
                // {
                //     git branch: "main",
                //     credentialsId: 'git',
                //     url: 'https://github.com/amitkshatriya01/selenium.git'
                //     sh 'mvn test'
                //     // withSonarQubeEnv(installationName: 'sonar') {
                //     //     sh 'mvn clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.0.2155:sonar'
                //     // }
                // }
                withSonarQubeEnv(installationName: 'sonar') {
                    sh 'sonar-scanner-5.0.1.3006-linux/bin/sonar-scanner -Dsonar.junit.testExecutionReportPaths=/target/results.xml'
                }
            }
        }
    }
}
 