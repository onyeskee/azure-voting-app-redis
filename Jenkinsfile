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
            
               docker build -t jenkins-pipeline .
               docker images -a
               cd ..   '''       
                
            
         }
      }
   }
}
