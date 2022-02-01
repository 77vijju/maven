pipeline {
    agent any

    stages {
        stage('Get_Code_ blaster') {
            steps {
                git 'https://github.com/AneesRavidKhan/DemoATC.git'
            }
        }
        stage('Build_Code') {
            steps {
                sh 'mvn install'
            }
        }
        stage('Deploy') {
            steps {
                sh 'sshpass -p "vijju" scp target/DemoATR.war vijju@172.17.0.4:/opt/apache-tomcat-9.0.56/webapps'
            }
        }
    }
}
