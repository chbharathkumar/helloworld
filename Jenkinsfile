pipeline {
    agent any
    tools {
        maven 'MVN_HOME'
        jdk 'JAVA_HOME'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    
                '''
            }
        }

        stage ('Build') {
            steps {
                sh 'mvn package' 
            }
        }
    }
    post { 
        always { 
            cleanWs()
        }
    }
}
