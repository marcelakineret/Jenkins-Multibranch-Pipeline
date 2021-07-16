pipeline {
    	agent any
           	stages {
                   	stage('Frist') {
                           	enviroment {
                                  	EXECUTE = 'true'                             	'
                           	}
                            steps {
                                    sh 'echo "Step One"'
                   	        }
                    }
                   	stage('Second') {
                           	when {
                                   enviroment name: "EXECUTE" , value: 'true'  	
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
