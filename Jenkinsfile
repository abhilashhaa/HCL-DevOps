pipeline {
    agent any 
    stages {
        stage('gctsCreateRepository') { 
            steps { 
              gctsCreateRepository script: this
                
            }
        }
        stage('gctsCloneRepository') { 
            steps {
                gctsCloneRepository script: this
            }
        }
        stage('gctsDeploy') { 
            steps {
                gctsDeploy script: this
            }
        }
    }
}



