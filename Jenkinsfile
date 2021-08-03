pipeline {
    agent any 
    stages {
        stage('CreateRepository') { 
            steps { 
              gctsCreateRepository
                
            }
        }
        stage('CloneRepository') { 
            steps {
                gctsCloneRepository
            }
        }
        stage('Deploy') { 
            steps {
                // 
            }
        }
    }
}



