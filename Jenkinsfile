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
        stage ( 'build my project' )
        {
            steps
            {
                sh 'mvn package' 
            }
        }
        stage ('deploy to tomcat')
        {
            steps
            {
                sshagent(['depliy-tomcat'])
                {
                    sh 'scp -o StrictHostKeyChecking=no **/*.war ec2-user@3.14.148.43:/var/lib/tomcat/webapps'
                }
            }
        }
    }
}
