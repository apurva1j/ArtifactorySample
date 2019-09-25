pipeline {
    agent any

    stages {
 stage('upload') {
           steps {
              script { 
                 def server = Artifactory.server 'frogArtifactory'
                 def uploadSpec = """{
                    "files": [{
                       "pattern": "C:\Apurva\Bars\",
                       "target": "SampleRepo"
                    }]
                 }"""

                 server.upload(uploadSpec) 
               }
            }
        }
    } 
}