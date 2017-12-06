properties([[$class: 'GithubProjectProperty', displayName: '', projectUrlStr: 'https://github.com/vineeth0310/multibranch.git/'], pipelineTriggers([githubPush()])])
pipeline {
    agent any 

    stages {
        stage(' Checkout Stage') { 
            steps { 
                sh 'ls' 
            }
        }
        stage('Build stage'){
            steps {
                sh 'pwd' 
            }
        }
        stage('starting database rebuild') {
            steps {
                sh 'ls'
            }
        }
    }
}
