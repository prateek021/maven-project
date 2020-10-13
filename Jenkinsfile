pipeline
{
    agent any
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
                withSonarQubeEnv(credentialsId: 'sonarqube-2') 
                {
                    sh 'mvn sonar:sonar package'
                }
            }
        }
    }
}
