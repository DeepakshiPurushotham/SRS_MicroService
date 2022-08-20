pipeline {
    agent any

tools {
  terraform 'Terraform_v1.2.7'
  }

stages{
    stage ('git checkout') {
      steps{
        git url: 'https://github.com/DeepakshiPurushotham/SRS_MicroService.git' , branch: 'master'
        }
      }
     }
stages {
    stage ('Terraform_init') {
      steps {
        sh "terraform init"
           }
         }
        }
stages {
     stage ('Terraform_Apply/Destroy') {
        steps {
          sh "terraform ${action} --auto-approve"
            }
         }
       }
}
