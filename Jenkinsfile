pipeline {
    agent any

    stages {
        stage('Get_Code_Master') {
            steps {
                git 'https://github.com/kliakos/sparkjava-war-example.git'
            }
        }
        stage('Build_Code') {
            steps {
                sh 'mvn install'
            }
        }
        stage('Deploy') {
            steps {
                sh 'sshpass -p "vijju" scp target/sparkjava-hello-world-1.0.war vijju@172.17.0.3:/opt/apache-tomcat-9.0.56/webapps'
            }
        }
    }
}
