pipeline {
    agent any

    stages {
        stage('Step 1: Get the Code') {
            steps {
                // This tells Jenkins to download YOUR specific GitHub repository
bat 'kubectl --kubeconfig="C:\\Users\\sande\\.kube\\config" apply -f .'            }
        }

        stage('Step 2: Deploy to Kubernetes') {
            steps {
                // First, Jenkins needs to open the specific folder where the YAML files live
                dir('k8s-specifications') {
                    
                    // Finally, Jenkins types the EXACT command the instructor typed!
                    bat 'kubectl apply -f .' 
                    
                }
            }
        }
    }
}
