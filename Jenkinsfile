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
				sh "ssh git@172.131.0.110:22 pwd"
			    sh  "pwd"	
                         
                        }catch(error){
                           
                        }
                    }
		     
		
	     }
	}
}
}
}
		
		        

		

					    

			 



  
	
