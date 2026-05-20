pipeline{
    agent any

    stages{
        stage('build image')
        {
                steps{
                    sh 'docker build -t docker-react .'
                }
        }
        stage('run container')
        {
            steps{
                sh 'docker run -d -p 5050:80 --name docker-reactC docker-react'
            }
        }
        stage('verify container')
        {
            steps{
                sh 'docker ps'
            }
        }
    }
}