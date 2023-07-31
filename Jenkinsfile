pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'rm -rf build'
                sh 'mkdir build' 
                sh 'touch build/car.txt'
                sh 'echo "chasis" > build/car.txt'
                echo 'hello'
            }
        }
        stage('Test'){
            steps {
                sh 'test -f build/car.txt'
                sh 'grep "chasis" build/car.txt'
                echo 'hello Mohan'
                echo 'chetan'
            }
        }
        stage('Publish'){
            steps{
                archiveArtifacts artifacts: 'build/'
            }
        }
    }
}
