pipeline
{
    agent 
    {
        node
        {
            label 'test_docker'
        }
    }
    stages
    {
        stage('build-step')
        {
            steps
            {
                echo 'code build successfully'
                sh '$x'
                git branch: 'master', url: 'https://github.com/vimallinuxworld13/simple-java-maven-app.git'
                sh 'mvn package'
            }
        }
        stage('test-code')
        {
            steps
            {
                echo 'code tested successfully'
                sh '$y'
            }
        }
        stage('deploy-code')
        {
            steps
            {
                echo 'code deployed successfully'
                sh '$z'
            }     
        }
    }
}
