pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            withAWS(credentials:'aws-static') {
            s3Upload(file:'index.html', bucket:'udacity-static', path:'/')
            }
        }
    }
}