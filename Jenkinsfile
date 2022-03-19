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
        stage('Parallel Task') {
            steps {
                parallel(
                       a: {
                          echo "This is branch a"
                         },
                       b: {
                          echo "This is branch b"
                         }
                      )
               } 
        }
        stage('Deploy') { 
            steps {
               sh 'sleep 4'
            }
        }
    }
}
