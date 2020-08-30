pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Read YAML..'
                checkout scm
                sh "ls"
                script{ datas = readYaml (file: 'test.yml') }

            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}