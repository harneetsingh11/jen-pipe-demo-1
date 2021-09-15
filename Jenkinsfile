pipeline
{
    agent none
    stages
    {
        stage('get_code')
        {
            agent
            {
                label 'get_code'
            }
            steps
            {
                echo 'code build successfully'
                sh '$x'
                git branch: 'master', url: 'https://github.com/vimallinuxworld13/simple-java-maven-app.git'
                stash includes: '*', name: 'code'
            }
        }
        stage('build_code')
        {
            agent
            {
                label 'build_code'
            }
            steps
            {
                echo 'code tested successfully'
                sh '$y'
                unstash 'code'
                sh 'mvn package'
                archive 'target/*.jar'
                stash includes: 'target/*.jar', name: 'package'
            }
        }
        stage('test_code')
        {
            agent
            {
                label 'test_code'
            }
            steps
            {
                echo 'code deployed successfully'
                sh '$z'
                unstash 'package'
                sh 'java -jar *jar'
            }     
        }
    }
}
