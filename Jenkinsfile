properties([[$class: 'GithubProjectProperty', displayName: '', projectUrlStr: 'https://github.com/vineeth0310/hooks/'], pipelineTriggers([githubPush()])])
properties([pipelineTriggers([upstream('master')])])

node {
 	// Clean workspace before doing anything
    deleteDir()

    try {
        stage ('clone') {
        	checkout scm
        }
        stage ('Build') {
        	sh "echo 'shell scripts to build the project nnn.....'"
		
        }
        stage ('Tests') {
	        parallel 'static': {
	            sh "echo 'shell scripts to run the static tests...'"
	        },
	        'unit': {
	            sh "echo 'shell scripts to run the unit tests...'"
	        },
	        'integration': {
	            sh "echo 'shell scripts to run integration tests...'"
	        }
        }
      	stage ('Deploy') {
            sh "echo 'shell scripts to deploy to server...'"
      	}
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
}
