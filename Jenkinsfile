pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Read YAML..'
                checkout scm
                sh "ls"
                echo "${env.WORKSPACE}"
                script{ datas = readYaml (file: "${env.WORKSPACE}/test.yaml") }

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