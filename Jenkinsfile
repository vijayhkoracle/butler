pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'echo "hello, world"'
            }
            input {
                    message "proceed?"
                    ok "yes"
                    parameters {
                        string(name: 'PERSON', defaultValue: 'Eric', description: 'name')
                    }
                }
            echo "Hello, ${PERSON}, nice to meet you"
        }
    }
}