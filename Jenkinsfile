pipeline{
    agent any

    tools{
        maven 'maven3'
    }

    stages{
        stage('clone'){
            steps{
                git 'https://github.com/PoorvikaK30/chatroom.git'
            }
        }
        stage('test'){
            steps{
                sh 'mvn clean compile'
            }
        }
        stage('test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('run the application'){
            steps{
                sh 'cd target && mv *.war /usr/local/tomcat/webapps/ROOT.war'
            }
        }
    }
}