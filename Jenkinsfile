pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t myimage 3docker'
      }
    }

    stage('Tag') {
      steps {
        sh 'docker tag myimage nandhurk27/myimage'
      }
    }

    stage('Push') {
      steps {
        sh 'docker push nandhurk27/myimage'
      }
    }

    stage('Deploy') {
      steps {
        sh 'docker run -d --name pipeline1 9001:80 nandhurk27/myimage'
      }
    }

  }
  environment {
    Name = 'Devops'
  }
}