pipeline {
      agent any
      stages {
        stage('Upload to AWS') {  
          steps {
            Use Jenkins UsernamePassword credentials information (Username: AccessKeyId, Password: SecretAccessKey):
            withAWS(credentials:'nameOfSystemCredentials') {
                s3Upload(file:'index.html', bucket:'jenkins-udacity-s3', path:'')
            }
          }
        }
      }
}
