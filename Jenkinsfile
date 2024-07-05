pipeline {
    agent any

    stages {
        stage('Deploy To Kubernetes') {
            steps {
                withKubeCredentials(kubectlCredentials: [[caCertificate: '', clusterName: 'eks-1', contextName: '', credentialsId: 'k8-token', namespace: 'webapps', serverUrl: 'https://C44600A4F6603C434911D06B3DFAAB87.gr7.us-east-1.eks.amazonaws.com']]) {
                    sh "kubectl apply -f deployment-service.yml"
                    sleep 60
                }
            }
        }
        
         stage('Deploy To Kubernetes') {
            steps {
                withKubeCredentials(kubectlCredentials: [[caCertificate: '', clusterName: 'eks-1', contextName: '', credentialsId: 'k8-token', namespace: 'webapps', serverUrl: 'https://C44600A4F6603C434911D06B3DFAAB87.gr7.us-east-1.eks.amazonaws.com']]) {
                    sh "kubectl get svc -n webapps "
                }
            }
        }
    }
}
