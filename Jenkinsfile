pipeline {
    agent none
    stages {
        stage('Checkout') {
           agent { label 'devopstest' } 
            
           steps {
               sh 'rm -rf hello-world-war'
             sh 'git clone https://github.com/Chethan170397/hello-world-war.git' 
            }
        }
        stage('Build') {
           agent { label 'devopstest' } 
            
           steps {
             sh 'mvn clean package' 
            }
        }
    }
}
