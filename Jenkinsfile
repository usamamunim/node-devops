pipeline {
  agent any
  stages {
    stage("build"){
      steps{
        script{
          docker.withRegistory(
            'https://934893693422.dkr.ecr.us-east-1.amazonaws.com',
            'ecr:us-east-1:b5d7207a-c9eb-4e13-bd12-684a8d7c1ac7'
          )
          {
            def myImage = docker.build('my-app')
            myImage.push('latest')
          }
        }
        echo "build stage is runing"      
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
