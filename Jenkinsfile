pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs' 
    }
    

    stages{
        stage('build'){
            steps{
                echo 'This is the build job'
                sh 'npm install'
            }
        }
        stage('test'){
            steps{
                echo 'This is the test job'
                sh 'npm test'
            }
        }
        stage('package'){
            steps{
                echo 'This is the package job'
                sh 'npm run package'
            }
        }
    }
    
    post{
        always{
            echo 'This is my first pipeline as code !'
        }
        
    }
    
}
