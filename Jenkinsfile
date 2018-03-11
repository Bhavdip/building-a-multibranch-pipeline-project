pipeline {
     agent { label 'master' }
     stages {
         stage('deploy') {
             steps {
                 retry(3) {
                    sh 'echo deploying...'
                 }
                 timeout(time: 10, unit: 'MINUTES') {
                    sh 'echo checking health...'
                 }            
             }
         }
     }
}