pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
/*    tools{
     	maven 'maven'
    }
*/    

    stages{
        stage('build'){
            steps{
                echo 'this is the build job'
                sh 'mvn compile'
                sleep 4
            }
        }
        stage('test'){
            steps{
                echo 'this is the second job'
                sh 'mvn clean test'
                sleep 9
            }
        }
        stage('package'){
            steps{
                echo 'this is the third job'
                sh 'mvn package -DSkipTests'
                sleep 7
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
