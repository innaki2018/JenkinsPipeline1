pipeline {
  
  agent any
 
  triggers {
         pollSCM('* * 24 02 *') 
  }

  stages{
        
   stage ('Run') {
        steps {
            sh 'echo "Today is `date`"'
            sh 'date >! /home/innaki/tmp/jenkins_was_here'
        }
        post {
            failure {
                sh 'echo "The Pipeline failed"'
            }
        }
        
   }

  }

    
    
}
