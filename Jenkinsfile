pipeline{
    agent any

    tools {nodejs "Node Installer"}

    stages{
        
        stage('Clone'){
           steps{
                echo "Cloning..."
                git 'https://github.com/fahad-git/pipeline_test.git'
               
           }
        }
 
        stage('Compiling'){
           steps{
                echo "Compiling..."
                sh "npm install"
           }
        }
        
        stage('Build'){
            steps{
                echo "Building..."
                sh "npm run build"
            }
        }

        stage('JUnit'){
            steps{
                echo "JUnit"
            }
        }
        
        stage('Deploy'){
            steps{
                echo "Deploying"
                sh "npm run dev"
                echo "Deployed Successfully"
            }
        }

    }
    
    post {
        
        always {
            echo "Always"
        }

        success {
            echo "Success"
        }

        failure {
            echo "Failure"
        }

        unstable {
            echo "Unstable"
        }

        changed {
            echo "Changed"
        }
    }
}
