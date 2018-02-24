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
                mail to: inna.kinevsky@gmail.com, subject: 'The Pipeline failed'
            }
        }
        
   }

  }

    
    
}
