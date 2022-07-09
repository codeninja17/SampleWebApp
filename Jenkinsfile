pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
               sh "mvn clean package"
            }
        }
        stage('Deployment') {
            steps {
               deploy adapters: [tomcat7(credentialsId: '57e0a381-fc59-44f3-a4ff-d85cf6528675', path: '', url: 'http://52.66.40.135:8080/')], contextPath: 'samplewebapp', war: '**/SampleWebApp.war'
            }
        }
    }
}
