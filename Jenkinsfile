pipeline {
    agent any
    tools {
        maven 'Maven3'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    withMaven(mavenSettingsConfig: 'my-nexus-settings', maven: 'Maven3') {
                        sh 'mvn clean deploy -DskipTests'
                    }
                }
            }
        }
    }
}