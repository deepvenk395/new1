pipeline{
    agent any
    stages{
        stage ("git"){
            steps{
                git branch: 'main', url: 'https://github.com/deepvenk395/new1.git'
                sh '''
                   sudo yum install httpd -y
                   sudo service httpd start
                   sudo cp -rf /var/lib/jenkins/workspace/python/index.html /var/www/html/
                   sudo service httpd restart
                   '''
            }
        }
    }
}
