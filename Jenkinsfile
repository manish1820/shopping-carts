pipeline
{
    agent any
  {
     	maven 'maven'
    }
 

    stages{
        stage('build')
       {
            steps{
                echo 'this is the build job'
                sh 'mvn compile'
               
            }
        }
        stage('test')
      {
            steps{
                echo 'this is the second job'
                sh 'mvn clean test'
                
            }
        }
        stage('package')
      {
            steps{
                echo 'this is the third job'
                sh 'mvn package -DSkipTests'
             
            }
        }
    }
    
    post{
        always
        {
            echo 'this pipeline has completed...'
        }
        
    }
    
