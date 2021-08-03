pipeline {
    agent any 
    stages {
        stage('gctsCreateRepository') { 
            steps { 
             gctsCreateRepository(
  script: this,
  host: 'https://hcluks4hana.hcldigilabs.com:8001',
  client: '000',
  abapCredentialsId: 'AbapSystem',
  repository: 'myrepo',
  remoteRepositoryURL: 'https://github.com/abhilashhaa/gCTS',
  role: 'SOURCE',
  vSID: 'FEF'
  )
                
            }
        }
        stage('gctsCloneRepository') { 
            steps {
               gctsCloneRepository(
  script: this,
  host: 'https://hcluks4hana.hcldigilabs.com:8001',
  client: '000',
  abapCredentialsId: 'AbapSystem',
  repository: 'myrepo'
)
            }
        }
        stage('gctsDeploy') { 
            steps {
                gctsDeploy script: this
                 host: 'https://hcluks4hana.hcldigilabs.com:8001',
  client: '000',
  abapCredentialsId: 'AbapSystem',
  repository: 'myrepo',
  remoteRepositoryURL: "https://github.com/abhilashhaa/gCTS",
  role: 'SOURCE',
  vSID: 'FEF',
  branch: 'master',
  commit: 'commit',
  scope: 'scope',
  rollback: false,
  configuration: [dummyConfig: 'dummyval']
)
            }
        }
    }
}



