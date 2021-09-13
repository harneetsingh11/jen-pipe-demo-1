pipeline
{
    agent none
    stages
    {
        stage('build-step')
        {
            agent
            {
                label 'test_docker'
            }
            steps
            {
                echo 'code build successfully'
                sh '$x'
                git branch: 'master', url: 'https://github.com/vimallinuxworld13/simple-java-maven-app.git'
               
            }
        }
        stage('test-code')
        {
            agent
            {
                label 'build_pac'
            }
            steps
            {
                echo 'code tested successfully'
                sh '$y'
                sh 'mvn package'
                archive 'target/*.jar'
            }
        }
        stage('deploy-code')
        {
            agent
            {
                label 'build_pac'
            }
            steps
            {
                echo 'code deployed successfully'
                sh '$z'
            }     
        }
    }
}
