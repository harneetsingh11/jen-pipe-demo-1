pipeline
{
    agent none
    stages
    {
        stage('build-step')
        {
            agent
            {
                label 'build_pac'
            }
            steps
            {
                echo 'code build successfully'
                sh '$x'
                git branch: 'master', url: 'https://github.com/vimallinuxworld13/simple-java-maven-app.git'
                sh 'mvn package'
                archive 'target/*.jar'
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
