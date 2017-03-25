pipeline{
    agent {
        label 'rhel'
    }

    stages{

        stage('Pull Repo'){
            steps {
                git 'https://github.com/asquarezone/spring-petclinic.git'
                
            }
        }

        stage('Build'){
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Publish'){
            junit allowEmptyResults: true, testResults: 'target/surefire-reports/*.xml'
        }
    }
}