pipeline{
    tools{
        maven'maven'
    }
    agent any
    stages {
        stage('Build') {
            steps {
                 bat 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
               bat 'mvn test'
            }
        }
        stage('Deliver') {
            steps {
               bat './scripts/deliver.bat'
            }
        }
    }
}