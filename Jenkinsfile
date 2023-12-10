node {
  docker.image('node:16-buster-slim') 
  docker.withRun('-p 3000:3000') {
    stage('Build') {
      sh 'npm install'
    }

    stage('Test') {
      sh './jenkins/scripts/test.sh'
    }
  }
}
