pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'echo "This is Build Step"'
                sh 'javac HelloWorld.java'
            }
        }
        stage('Test') { 
            steps {
                sh 'echo "This is execute step"'
                sh 'java HelloWorld'
                sh 'exit 0'
            }
        }
        stage('Deploy') { 
            steps {
               sh 'sleep 4'
            }
        }
    }
}
