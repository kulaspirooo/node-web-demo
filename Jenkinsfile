pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Building Node.js app..."'
      }
    }
    stage('Deploy to Kubernetes') {
      steps {
        sh 'microk8s kubectl apply -f k8s_deployment.yaml'
        sh 'microk8s kubectl apply -f k8s_service.yaml'
      }
    }
  }
}
