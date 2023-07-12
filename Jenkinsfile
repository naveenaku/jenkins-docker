pipeline {
  agent any
  stages {
    stage('Docker Build') {
      steps {
        sh '''
          docker build -t jenkins-docker .
        '''
      }
    }
    stage('K8s Deploy') {
      steps {
        sh '''
          kubectl apply -f deploymentservice.yaml
        '''
      }
    }
  }
}
