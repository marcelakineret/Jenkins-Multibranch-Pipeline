pipeline {
    	agent any
               	stages {
                       	stage('Frist') {
                                   steps {
                                          sh 'echo "Step One"'
                                          script {
                                              env.EXECUTE = "True"
                                          }
                                          echo "${EXECUTE}"
                   	               }
                        }
                   	    stage('Second') {
                                   when {
                                       env.EXECUTE, value: "True"
                                   }
                                   steps { 
                                           sh 'echo :"Updaiting" Second Stage"' 
                           	       }
                        }
                        stage('Thrird') {
                                    when {
                                       env.EXECUTE, value: "False"
                                    }
                                    steps {
                                  	        sh '
                                                 echo "Step Three"
                                               '                                  	
                                    }
                   	    }
           	      }
}
