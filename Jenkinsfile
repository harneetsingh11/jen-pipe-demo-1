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
                sh 'sleep 5'
            }
        }
        stage('test-code')
        {
            steps
            {
                echo 'code tested successfully'
                sh 'sleep 5'
            }
        }
        stage('deploy-code')
        {
            steps
            {
                echo 'code deployed successfully'
                sh 'sleep 5'
            }     
        }
    }
}
