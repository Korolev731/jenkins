pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('step2') {
            steps {
                script {
                def response = input message: 'what? ',
                parameters: [choice(choices: 'YES\nNO' ,
                description: 'sdf?',
                name: 'What to do?')]
                
                sh 'git --version'
                echo env.JOB_NAME
                echo env.JENKINS_HOME                
            
                }
                }
        }
        stage('step3') {
            steps {
                echo 'Hello World'
            }
        }
    
        stage('step4') {
            steps {
                sh '''
                env | grep -e PATH -e JAVA_HOME
                which java
                java -version
                
                
                '''
            }
        }
    }
    
}
