pipeline {
    agent any 
    stages {
        stage('CreateRepository') { 
            steps { 
              gctsCreateRepository script: this
                
            }
        }
        stage('CloneRepository') { 
            steps {
                gctsCloneRepository script: this
            }
        }
        stage('Deploy') { 
            steps {
                gctsDeploy script: this
            }
        }
    }
}



