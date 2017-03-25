pipeline{
    agent any

    stages{

        stage('Pull Repo'){
            steps {
                git 'https://github.com/asquarezone/spring-petclinic.git'
                
            }
        }

        stage('Build'){
            steps {
                sh 'cd spring-petclinic'
                sh 'mvn clean install'
            }
        }
    }
}