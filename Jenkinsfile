pipeline {

    agent any


    stages {

        stage('Build code') {
            steps {
                     checkout scm
                sh '''
		  cd ..
		  zip --exclude '*.git*' -r nodejs-v1.zip samplenodejs-ebs
                '''
            }

        }

        stage('Execute test code') {
         steps {
        sh '''
		echo "Running test case now"
           '''
         }
        }
        }

        stage('Test') {
        steps {
        sh '''
          echo "Push is going on"
           '''
        }
        }

        stage('Deploy code to elasticbeanstalk') {
        steps {
        sh '''
	    eb deploy --staged
           '''
        }
        }

