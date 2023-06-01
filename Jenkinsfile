pipeline {
  agent any
  stages {
    stage('Deploy') {
      steps {
        echo "Deploying to S3 bucket"
        sh 'aws s3 cp . s3://portfolio-nischal-bucket-v1 --recursive'
      }
    }
  }

  post {
    success {
      echo "success"
    }
    failure {
      echo "failure"
    }
  }
}