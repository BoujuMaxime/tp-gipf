pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './gradlew -D https.proxyHost=proxy1-rech -D https.proxyPort=3128 compileJava'
            }
        }
        stage('Test') {
            steps {
                sh './gradlew -D https.proxyHost=proxy1-rech -D https.proxyPort=3128 test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
