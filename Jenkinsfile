@Library('piper-library-os') _

pipeline {
    agent any 
    stages {
        stage('gctsCreateRepository') { 
            steps { 
             gctsCreateRepository
  script: this,
  host: 'https://hcluks4hana.hcldigilabs.com:8001',
  client: '000',
  abapCredentialsId: 'AbapSystem',
  repository: 'HCL_Github',
  remoteRepositoryURL: 'https://github.com/abhilashhaa/HCL_Githup',
  role: 'SOURCE',
  vSID: 'FEF'
  
                
            }
        }
        stage('gctsCloneRepository') { 
            steps {
               gctsCloneRepository
  script: this,
  host: 'https://hcluks4hana.hcldigilabs.com:8001',
  client: '000',
  abapCredentialsId: 'AbapSystem',
  repository: 'HCL_Github'

            }
        }
        stage('gctsDeploy') { 
            steps {
                gctsDeploy script: this
                 host: 'https://hcluks4hana.hcldigilabs.com:8001',
  client: '000',
  abapCredentialsId: 'AbapSystem',
  repository: 'myrepo',
  remoteRepositoryURL: "https://github.com/abhilashhaa/HCL_Githup",
  role: 'SOURCE',
  vSID: 'FEF',
  branch: 'master',
  commit: 'commit',
  scope: 'scope',
  rollback: false,
  configuration: [dummyConfig: 'dummyval']

            }
        }
    }
}



