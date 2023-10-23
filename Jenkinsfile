pipeline {
    agent none
    parameters { string(name: 'PARAM1', description: 'Param 1?') 
                string(name: 'PARAM2', description: 'Param 2?') 
               
choice( name: 'CHOICE', choices: ['one', 'two', 'three'], description: '' )
               }
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
