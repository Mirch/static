pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            dir('/'){
                pwd();

                withAWS(region:'us-west-2', credentials:'aws-static') {
                    def identity = awsIdentity();

                    s3Upload(file:'index.html', bucket:'udacity-static', path:'/')
                }
            }
        }
    }
}