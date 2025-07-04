pipeline {
    agent any
    tools {
            maven 'Maven3'
     }
    stages {
        stage('Build') {
            steps {
             script {
                withMaven(mavenSettingsConfig: 'my-nexus-settings', maven: 'Maven3') { // 替换为你的 Maven 安装名称
                    sh 'mvn clean deploy -DskipTests' // 执行 Maven 命令，它会使用注入的 settings.xml
                }
            }
        }
    }
}