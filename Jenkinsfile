pipeline {
    	agent any
           	stages {
                   	stage('Frist') {
                           	enviroment {
                                  	EXECUTE = 'True'                             	'
                           	}
                            steps {
                                    sh 'echo "Step One"'
                   	        }
                    }
                   	stage('Second') {
                           	when {
                                   enviroment name: "EXECUTE" , value: 'True'  	
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
