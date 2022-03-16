pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs' 
    }    

    stages{
        stage('compile'){
            steps{
                echo 'this is the Compilation job'
                sh 'npm install'
            }
        }
        stage('test'){
            steps{
                echo 'this is the Testing job'
                sh 'npm test'
            }
        }
        stage('package'){
            steps{
                echo 'this is the Packaging job'
                sh 'npm run package' 
            }
        }
    }
    
    post{
        always{
            echo 'This Pipeline has completed...'
        }
        
    }
    
}
