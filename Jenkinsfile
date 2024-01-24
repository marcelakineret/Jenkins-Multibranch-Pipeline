pipeline {
    	agent any
               	stages {
                       	stage('Frist') {
                                   steps {
                                         environment { EXECUTE = 'true'   }
                                          sh 'echo "Step One"'
                                                      }
                        }
                   	    stage('Second') {
                                   when {
                                         environment name: 'EXECUTE', value: 'true'
                                   }
                                   steps { 
                                           sh 'echo :"Updaiting" Second Stage"' 
                           	       }
                        }
                        stage('Thrird') {
                                    when {
                                         environment name: 'EXECUTE', value: 'false'
                                    }
                                    steps {
                                  	        sh 'echo "Step Three"'                                  	
                                    }
                   	    }
           	      }
}
