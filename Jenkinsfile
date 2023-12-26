node{
  stage("Checkout"){
        git branch: 'react-app', url: 'https://github.com/Cydnirn/dicoding-cicd-labs'
    }
  withDockerContainer(args: '-p 3000:3000', image: 'node:16-buster-slim'){
    stage('Build') {
      sh "ls"
      sh 'npm install'
    }

    stage('Test') {
      sh './jenkins/scripts/test.sh'
    }
  }
}
