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
                dspComponent = "security_services"
                echo yamlData.components."${dspComponent}".component_user.toString()

            }
        }
    }
}