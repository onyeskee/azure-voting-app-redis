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
            sh label: '', script: '''   ~/Library/Containers/com.docker.docker/Data/vms/0           
               docker images -a              
               cd azure-vote/
               docker images -a
               cd .. '''
            
         }
      }
   }
}
