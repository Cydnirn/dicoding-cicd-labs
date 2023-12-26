node{
  stage("Checkout"){
        git branch: 'react-app', url: 'https://github.com/Cydnirn/dicoding-cicd-labs'
    }
  docker.image("node:16-buster-slim").inside("-p 3000:3000"){
    stage('Build') {
      sh "ls"
      sh 'npm install'
    }

    stage('Test') {
      sh './jenkins/scripts/test.sh'
    }
  }
}
