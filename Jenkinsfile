pipeline {
    agent any
    stages {
	stage('Pre-build'){
	    steps {
	    	echo 'Pre-build'
	    	sh 'sleep 2'
	    }
	}
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
	
    }
}
