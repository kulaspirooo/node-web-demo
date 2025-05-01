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
        sh 'kubectl apply -f k8s_deployment.yaml'
        sh 'kubectl apply -f k8s_service.yaml'
      }
    }
  }
}
