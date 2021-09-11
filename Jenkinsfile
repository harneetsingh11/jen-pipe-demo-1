pipeline
{
    agent any
    stages
    {
        stage('build-step')
        {
            steps
            {
                echo 'code build successfully'
                sh '$x'
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
