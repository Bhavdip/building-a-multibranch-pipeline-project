pipeline {
    /* Multiple Steps 
    agent { label 'master' }
    stages {
       stage('build') {
          steps {
             sh 'echo step1'
             sh 'echo step2'
             sh '''
                echo 'Multiline'
                echo 'Example'
             '''
             echo 'not using shell'
          }
       }
    } */

    pipeline {
     agent { label 'master' }
     stages {
         stage('deploy') {
             steps {
                 retry(3) {
                    sh 'echo deploying...'
                 }
                 timeout(time: 3, unit: 'MINUTES') {
                    sh 'echo checking health...'
                 }            
             }
         }
     }
}

}