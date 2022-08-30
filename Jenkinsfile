pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage("Git checkout"){
            steps {
            git branch: 'main',
                url: 'https://github.com/pranavh00/Backbase.git'

            sh "ls -lat"
            }
        }
        stage("docker build"){
            steps{                     
	            sh 'sudo docker build -t pranav_tomcat:$BUILD_NUMBER .'     
	            echo 'Build Image Completed'                
            }  
        }
    }  
}
