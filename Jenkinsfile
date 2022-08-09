pipeline {
    agent any
    
    tools {
        gradle 'Gradle-7.5'
    }
    
    stages {
        stage("run frontend") {
            steps {
                echo 'executing yarn...'
                nodejs('Node-10.17') {
                    sh 'npm install'
                }
            } 
        }
        stage("run backend") {
            steps {
                echo 'executing gradle...'
                sh './gradlew -v'
            } 
        }
    }
}
