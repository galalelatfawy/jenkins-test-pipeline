node {

 stage ('Checkout')

    git 'https://github.com/galalelatfawy/jenkins-test-pipeline.git' 

 stage ('Build Docker Image')
      GIT_COMMIT_ID = sh (
    script: 'echo $(git rev-parse HEAD)',
    returnStdout: true
     ).trim()
    sh label: '', script: ' docker build -t  testbuild:dev_${GIT_COMMIT_ID} .'

//  stage('Push Docker Image With Commit ID To ECR')

//   docker.withRegistry('https://982712.dkr.ecr.eu-central-1.amazonaws.com', 'ecr:eu-central-1:jenkins-aws-id') {
//   docker.image(" 98.dkr.ecr.eu-central-1.amazonaws.com/marketspace:dev_${GIT_COMMIT_ID}").push("dev-${GIT_COMMIT_ID}")
//   }
//  stage ('change context')

//  sh ("kubectl config use-context arn:aws:eks:eu-central-1:wsdfsdf:cluster/nonprod-eks-fn")

//  stage ('Deploy to Staging Enviroment')

//   sh ("kubectl -n=dev set image deployment/fn-marketspace-dev marketspace-dev=sdf.dkr.ecr.eu-central-1.amazonaws.com/marketspace:dev_${GIT_COMMIT_ID}")

//  }
}