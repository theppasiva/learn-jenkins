pipeline {
    agent {
    node {
        label 'AGENT-1'
        
    }
    
}
    environment { 
        GRRETING = 'Hello Jenkins'
    }
    // Build
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                    echo "Here I wrote shell script"
                    echo ""$GRRETING
                """
            }
        }
    }
    // post build
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'this runs when pipeline is failed, used generally to send some alerts'
        }
        success { 
            echo 'I will  say Hello when pipeline is success!'
        }
    }
}