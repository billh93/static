pipeline {
      agent any
      stages {
        stage('Upload to AWS.') {
          steps {
            withAWS(region:'us-east-1', credentials:'IDofAwsCredentials') {
                AWSAccessKey: 'AKIAQH75HXAHBUKYWBPB', 
                AWSSecretKey: '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',
                s3Upload(file:'index.html', bucket:'jenkins-udacity-s3', path:'index.html')
            }
          }
        }
      }
}
