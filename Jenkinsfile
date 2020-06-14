pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('Docker Images') {
         steps { 
            sh label: '', script: '''   /var/lib/docker/volumes/jenkins_home/_data          
               docker images -a              
               cd azure-vote/
               docker images -a
               cd .. '''
            
         }
      }
   }
}
