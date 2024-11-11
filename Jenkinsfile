pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url:'https://github.com/Mohamed-Abonazel/pipline-task.git'  // Replace with your repository URL
            }
        }
        stage('Run my script') {
            steps {
                script {
                    // Assuming the 'myscript.sh' script is in the root of the repository
                     sh 'chmod +x myscript.sh'  // Make the script executable (if not already)
                     sh './myscript.sh'          // Run the  myscript.sh
                }
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
