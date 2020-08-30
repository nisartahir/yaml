pipeline {
    agent any

    stages {
        stage('Test Yaml') {
            steps {
                echo 'Read YAML..'
                checkout scm
                sh "ls"
                echo "${env.WORKSPACE}"
                script{ yamlData = readYaml (file: "${env.WORKSPACE}/test.yaml") }
                echo yamlData.components.security_services.component_user.toString()

            }
        }
    }
}