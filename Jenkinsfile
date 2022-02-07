pipeline{
    agent any
    stages
    {
        stage('checkout from SCM')
        {
            steps
            {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'yakhub-git', url: 'https://github.com/yakhub4881/python-file.git']]])
            }
        }

        stage('execute python script')
        {
            steps{
                sh 'python test.py'
            }
        }
    }
}
