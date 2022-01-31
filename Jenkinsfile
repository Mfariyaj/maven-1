pipeline {
    agent any

    stages {
        stage('Get_Code_Master') {
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
                sh 'sshpass -p "1234" scp target/DemoATR.war root@172.17.0.3:/opt/apache-tomcat-9.0.58/webappss'
            }
        }
    }
}
