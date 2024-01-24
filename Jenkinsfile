pipeline {
    	agent any
               	stages {
                       	stage('Frist') {
                                   steps {
                                          sh 'echo "Step One"'
                                          script {
                                              env.EXECUTE = "true"
                                          }
                                          echo "${env.EXECUTE}"
                   	               }
                        }
                   	    stage('Second') {
                                   when {iro
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
