pipeline {
  agent any
  stages {
    stage("build") {
      steps {
        script {
          docker.withRegistry(
            'https://934893693422.dkr.ecr.us-east-1.amazonaws.com',
            'us-east-1'
          ) {
            def myImage = docker.build('my-app')
            myImage.push('latest')
          }
        }
      }
    }
    stage("test"){
      steps{
        echo "test stage is running"      
      }
    }
    stage("deploy"){
      steps{
        echo "deploy stage is running"      
      }
    }
  }
}
