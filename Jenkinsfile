pipeline {
      agent any
      stages {
        stage('Upload to AWS.') {
          Use Jenkins UsernamePassword credentials information (Username: AccessKeyId, Password: SecretAccessKey):    
          steps {
            withAWS(credentials:'nameOfSystemCredentials') {
                s3Upload(file:'index.html', bucket:'jenkins-udacity-s3', path:'')
            }

            Use profile information from ~/.aws/config:
            withAWS(profile:'myProfile') {
                s3Upload(file:'index.html', bucket:'jenkins-udacity-s3', path:'')
            }
          }
        }
      }
}
