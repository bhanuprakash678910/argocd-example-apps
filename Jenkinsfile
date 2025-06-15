pipeline {
 agent {
  label 'k8s-agent'
}
stages {
 stage("init"){
  steps{
   
   git 'https://github.com/bhanuprakash678910/argocd-example-apps.git'

       }
   }
   stage("connection to k8s cluster"){
  steps{
   sh 'aws eks update-kubeconfig --region us-east-1 --name ekscluster'
       }
   }
   stage("deploying"){
  steps{
      
      sh '''cd helm-guestbook
helm install myrel .'''

       }
   }

  }
}
