pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo 'Clarusway_Way to Reinvent Yourself'
                sh 'echo Integrating Jenkins Pipeline with GitHub Webhook using Jenkinsfile'
            }

        stage('Build-1') {
            steps {
                sh 'echo "hello world"'
                sh '''
                echo $name
                echo $url
                echo "ilk step"
                sleep 5
                '''
            }
            when{
                environment name: 'name', value: 'test'
            }
        }
        stage('Build-2') {
            steps {
                sh 'echo "hello world"'
                sh '''
                echo $name
                echo $url
                echo "ikinci step"
                sleep 10
                '''
            }
            when{
                environment name: 'name', value: 'production' 
            }
        }
        stage('Build-4') {
            steps {
                sh 'echo "hello world"'
                sh '''
                echo $name
                echo $url
                echo "ilk step"
                sleep 15
                '''
            }
            when{
                environment name: 'name', value: 'test'
            }
        }
        stage('Build-3') {
            parallel {
                stage('Paralel1'){
                    steps {
                        sh '''
                        echo 'ilk paralel'
                        sleep 10 '''
                    }
                }
                stage('Paralel2'){
                    steps {
                        sh '''
                        echo 'ilk paralel'
                        sleep 25 '''
                    }
                }
            }
        }        
    }
    post {
        success {
            sh '''
            echo "Hello World"
            echo "post ${name}"
            '''
        }


            
        }
    }
}
