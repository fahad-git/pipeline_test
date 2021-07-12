pipeline{
    agent any

    tools {nodejs "Node Installer"}

    stages{
        
        stage('Clone'){
           steps{
                echo "Cloning..."
                git 'https://github.com/fahad-git/pipeline_test.git'
                sh "ls"
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
        
        stage('Testcases'){
            steps{
                echo "Other Testcases"
            }
        }
        
        stage('Quality-Gate'){
            steps{
                echo "Tesing...'"
            }
        }

        stage('Deploy'){
            steps{
                echo "Deploying"
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
