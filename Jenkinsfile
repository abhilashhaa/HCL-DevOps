@Library('piper-library-os') _

node()
{
stage('RunUnitTest') 
    gctsExecuteABAPUnitTests(
      script: this,
      host: 'https://hcluks4hana.hcldigilabs.com:8001',
      client: '200',
      abapCredentialsId: 'AbapSystem',
      repository: 'OpenSAP'
)

stage('RollbackCommit')
    {
        when{ 
            expression{<whatever>=='FAILURE'}
                      }
            steps{  
                script {
                gctsRollback(
                    
                script: this,
                host: "https://hcluks4hana.hcldigilabs.com:8001/",
                client: "200",
                abapCredentialsId: 'AbapSystem',
                repository: "OpenSAP"
  )
            }
            }

}
