pipeline {
    agent any
    parameters {
        choice(name: 'UbuntuRelease', choices: ['18.10', '19.04'], description: 'Chose Ubuntu Release')
               }
    stages {
        stage('build') {
            input {
                    message "proceed?"
                    ok "yes"
                    parameters {
                        string(name: 'PERSON', defaultValue: 'Eric', description: 'name')
                    }
                }
     
            steps {
                sh 'echo "Hello, ${PERSON}, nice to meet you on ${params.UbuntuRelease}"'
                sh 'chmod +x app.sh'
                sh label: '', script: './app.sh'
            }
        }
    }
}
