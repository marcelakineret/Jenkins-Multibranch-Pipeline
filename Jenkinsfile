pipeline {
    	agent any
	        stages { 
		    	stage('Frist') { 
						steps {
							sh ' echo "Step One" '
							script {
								env.EXECUTE = "True"
								}
							echo "${EXECUTE}"
							}	
				     }		
			stage('Second ') {
						when {
							environment name: 'EXECUTE', value: "True"
						     }
						steps { 
							sh ' echo "Step Two" '
							sh ' echo "Updating Second Stage" '	
						      }
				}
			stage('Thrird') {
						when {
							environment name: 'EXECUTE', value: "False"
						     }
						steps {
							sh ' echo "Step Three" '
						      }
				       }
			}
}
