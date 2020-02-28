pipeline {
	
	environment {
    GIT_URL="https://github.com/MishraKD/assignment11.git"
   
}
	
agent any	
	stages{
            
stage('DeployToProduction') {
	
             steps {
		     sshagent(['cd03b339-0eb5-462a-95e8-7903536ffb9a']) {
                    script{
                        try{
                            sh "ssh -tt git@172.31.0.110"
			    sh  "pwd"
                        }catch(error){
                            sh "ssh -tt git@52.214.113.246"
                        }
                    }
		     
		
	     }
	}
}
}
}
		
		        

		

					    

			 



  
	
