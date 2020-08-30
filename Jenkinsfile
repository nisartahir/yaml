pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Read YAML..'
                checkout scm
                script{ 
                    ls 
                    datas = readYaml (file: 'test.yml')
                     }

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