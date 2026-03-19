pipeline {
    agent any

    stages {
        stage('Step 1: Get the Code') {
            steps {
                // This tells Jenkins to download YOUR specific GitHub repository
                git branch: 'master', url: 'https://github.com/Sandeep3245/example-voting-app.git'
            }
        }

        stage('Step 2: Deploy to Kubernetes') {
            steps {
                // First, Jenkins needs to open the specific folder where the YAML files live
                dir('k8s-specifications') {
                    
                    // Finally, Jenkins types the EXACT command the instructor typed!
                    sh 'kubectl apply -f .' 
                    
                }
            }
        }
    }
}
