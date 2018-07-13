pipeline { 
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
                awsCodeBuild projectName: 'jenkins_generic', credentialsType: 'keys', region: 'us-east-2', sourceControlType: 'jenkins'
                sh 'echo "Unit testing compiled libraries..."'
            }
        }
        stage('Deployment'){
            steps {
                sh 'echo "Releasing to customers"'
            }
        }
    }
}
