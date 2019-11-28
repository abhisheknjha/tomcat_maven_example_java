pipeline {
	agent any

	stages {
	stage('build servelet project') {
	steps {
	sh 'mvn clean package'
	}

	post{
	success{
	echo 'now Archiving..'

	archiveArtifacts artifacts : '**/*.war'
	}
	}
	}
	}
}
