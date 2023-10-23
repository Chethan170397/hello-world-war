pipeline {
    agent { label 'devopstest' }
    stages {
        stage('Checkout') {
            
            
           steps {
               sh 'rm -rf hello-world-war'
             sh 'git clone https://github.com/Chethan170397/hello-world-war.git' 
            }
        }
        stage('Build') {
            
            
           steps {
             sh 'mvn clean package' 
            }
        }
    }
}
