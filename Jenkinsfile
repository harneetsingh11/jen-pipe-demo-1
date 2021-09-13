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
                git branch: 'main', url: 'https://github.com/harneetsingh11/demo-git.git'
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
