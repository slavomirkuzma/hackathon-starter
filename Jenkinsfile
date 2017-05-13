pipeline {
    agent { dockerfile true }
    stages {
        stage('Stage on node') {
			steps {
                echo 'Running stage in node docker.'
                sh 'node --version'
            }
		}
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
        }
    }
}