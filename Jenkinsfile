pipeline {
	
	environment {
    GIT_URL="https://github.com/MishraKD/assignment11.git"
   
}
	
agent any	
	stages{
            
stage('DeployToProduction') {
	
             steps {
		     sshagent(['kops-machine']) {
                    script{
                        try{
                            sh "ssh -A git@52.214.113.246:22"
			    sh  "pwd"
                        }catch(error){
                            sh "ssh -A git@52.214.113.246:22 "
                        }
                    }
		     
		
	     }
	}
}
	}	
	}
		
		        

		

					    

			 



  
	
