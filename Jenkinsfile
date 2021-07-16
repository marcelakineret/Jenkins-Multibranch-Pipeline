pipeline {
    	agent any
           	stages {
                   	stage('Frist') {
                           	environment {
                                  	EXECUTE = 'true'                             	'
                           	}
                            steps {
                                    sh 'echo "Step One"'
                   	        }
                    }
                   	stage('Second') {
                           	when {
                                   environment name: "EXECUTE" , value: 'true'  	
                                   steps { 
                                   sh 'echo :"Updaiting" Second Stage"
                           	     }
                            }
                        
                    }    
                   	stage('Thrird') {
                           	steps {
                                  	sh 'echo "Step Three"'                                  	'
                           	}
                   	}
           	}
}
