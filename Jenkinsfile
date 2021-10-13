pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t apache_pipeline Docker'
      }
    }

    stage('Tag') {
      steps {
        sh 'docker tag apache_pipeline nandhurk27/apache_pipeline'
      }
    }

    stage('Push') {
      steps {
        sh 'docker push nandhurk27/apache_pipeline'
      }
    }

    stage('Deploy') {
      steps {
        sh 'docker run -d --name pipeline1 9001:80 nandhurk27/apache_pipeline'
      }
    }

  }
  environment {
    Name = 'Devops'
  }
}