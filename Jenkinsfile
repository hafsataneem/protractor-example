pipeline {
    agent any
    stages {
        stage("Checkout code") {
            steps {
                //snDevOpsStep()
                checkout scm
            }
        }
        stage("Build and test") {
            steps {
                //snDevOpsStep()
                npm install
                npm test
            }
            post {
       		   always {
          		    junit '**/build/reports/e2e/*.xml'
        	    }
            }
        }       
    }    
}