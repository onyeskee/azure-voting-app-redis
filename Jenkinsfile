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
            sh label: '', script: '''             
               docker images -a              
               cd azure-vote/
               docker images -a
               cd .. '''
            
         }
      }
   }
}
