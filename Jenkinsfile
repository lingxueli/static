pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				withAWS(region:'us-west-2', credentials:'aws-static') {
					s3Upload(file:'index.html', bucket:'jenkins-us-west-2-lisa-marie', path:'index.html')
				}
			}
		}
	}
}
