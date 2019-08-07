pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            withAWS(region:'us-west-2', credentials:'aws-static') {
            s3Upload(file:'index.html', bucket:'udacity-static', path:'/')
            }
        }
    }
}