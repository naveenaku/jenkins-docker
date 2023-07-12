pipeline {
  agent any
  stages {
    stage('Docker Build') {
      steps {
        sh '''
          docker build -t naveenakula029/jenkins-docker .
          docker push naveenakula029/jenkins-docker
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
