pipeline { 
    agent any 
    stages {
        stage('Build'){
            steps {
                sh 'echo "Compiling..."'
            }
        }
        stage('Test'){
            steps {
                sh 'echo "Unit testing compiled libraries..."'
            }
        }
        stage('Preflight'){
            steps {
                sh 'echo "Running external test battery from QA"'
            }
        }
        stage('Deployment'){
            steps {
                sh 'echo "Releasing to customers"'
            }
        }
    }
}
