pipeline
{
    agents any
    stages
    {
        stage ('scm checkout')
        {
            steps 
            {
                git 'https://github.com/prateek021/maven-project'
            }
        }
        stage ('build the project along with sonar')
        {
            steps
            {
                sh 'sonar:sonar package'
            }
        }
    }
}
