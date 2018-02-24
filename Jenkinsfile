pipeline {
  
  agent any
 
  triggers {
         pollSCM('* * 24 02 *') 
  }

  stages{
        
   stage ('Run') {
        steps {
            sh 'echo "Today is `date`"'
            sh '`date` >! /tmp/jenkins_was_here'
        }
        post {
            failure {
                sh 'echo "The Pipeline failed"'
            }
        }
        
   }

  }

    
    
}
