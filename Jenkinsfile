pipeline {
     agent any
     stages {
         stage('Upload to AWS') {
              steps {
                  withAWS(region:'eu-central-1',credentials:'test-aws') {
                      s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'app.py', bucket:'my-storage-test-1')
                  }
              }
         }
     }
}
