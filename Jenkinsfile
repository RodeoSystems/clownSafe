pipeline { 
    awsCodeBuild projectName: 'project', credentialsType: 'keys', region: 'us-west-2', sourceControlType: 'jenkins'
    agent any 
    stages {
        stage('Build'){
            steps {
                sh 'echo "Compiling..."'
		sh 'echo "Building for Embedded Target 1"'
		sh 'echo "Building for Embedded Target 2"'
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
