pipeline{

    agent any

tools{
       nodejs 'nodejs' 
    }
    

    stages{
        stage('build-the-app'){
            steps{
                echo 'this is the first job'
                sh 'npm install'
               }
        }
        stage('test-the-app'){
            steps{
                echo 'this is the second job'
                sh 'npm test'
              
            }
        }
        stage('package-the-app'){
            steps{
                echo 'this is the third job'
                sh 'npm run package'
                
            }
        }
    }
    
    post{
        always{
            echo 'this is my first pipeline as code...'
        }
        
    }
    
}
