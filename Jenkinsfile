pipeline {
    	agent any
               	stages {
                       	stage('Frist') {
                                   steps {
                                          sh 'echo "Step One"'
                                          script {
                                              env.EXECUTE = "True"
                                          }
                                          echo "${env.EXECUTE}"
                   	               }
                        }
                   	    stage('Second') {
                                   when {
                                       enviroment name: 'EXECUTE', value: "True"
                                   }
                                   steps { 
                                           sh 'echo :"Updaiting" Second Stage"' 
                           	       }
                        }
                        stage('Thrird') {
                                    when {
                                       enviroment name: 'EXECUTE', value: "False"
                                    }
                                    steps {
                                  	        sh 'echo "Step Three"'                                  	'
                                    }
                   	    }
           	      }
}
