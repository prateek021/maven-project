pipeline
{
    agent any
    stages
    {
        stage ( 'clone from git' )
        {
            steps
            {
                git branch: 'master', url: 'https://github.com/prateek021/maven-project'
            }
        }
        stage ( 'compile my project' )
        {
            steps
            {
                  sh 'mvn compile' 
            }
        }
    }
}
