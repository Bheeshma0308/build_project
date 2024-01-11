pipeline
{
    agent any
    tools
    {
        maven 'MAVEN'
    }
    environment 
    {
        MAVEN_GOALS = 'mvn -Dmaven.test.failure.ignore=true clean package'        // Define the Maven goals for building the project  
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
