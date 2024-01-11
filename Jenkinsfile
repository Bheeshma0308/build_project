pipeline
{
    agent any
    
    environment 
    {
        MAVEN_GOALS = 'maven -Dmaven.test.failure.ignore=true clean package'        // Define the Maven goals for building the project  
    }
    stages
    {
        
        stage('Build')
        {
            steps
            {
                 sh "mvn ${MAVEN_GOALS}"
            }
        }
    }
    post
    {
        success
        {
            echo "Build successful!"
        }
        failure 
        {
            echo "Build failed!"
        }
    }
}
