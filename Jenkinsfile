pipeline {
      agent any
      stages {
        stage('Upload to AWS.') {
          steps { 
            withAWS(credentials:'awscredentials') {
                s3Upload(file:'index.html', bucket:'jenkins-udacity-s3', path:'')
            }
          }
        }
      }
}
