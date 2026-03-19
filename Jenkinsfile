pipeline {
    agent any

    stages {
        stage('Step 1: Get the Code') {
            steps {
                // This downloads your code from GitHub
                git branch: 'master', url: 'https://github.com/Sandeep3245/example-voting-app.git'
            }
        }

        stage('Step 2: Deploy to Kubernetes') {
            steps {
                dir('k8s-specifications') {
                    // This tells kubectl to use your new Minikube cluster
                    bat 'kubectl --kubeconfig="C:\\Users\\sande\\.kube\\config" --context=minikube apply -f .' 
                }
            }
        }
    }
}
