pipeline {
	
	environment {
    GIT_URL="https://github.com/MishraKD/assignment11.git"
   
}
	
agent any	
	stages{
            
stage('DeployToProduction') {
	
             steps {
		      
		     
		kubernetesDeploy(
                    kubeconfigId: 'kubeconfiggit',
                    configs: 'deploymentfile.yml',
                    enableConfigSubstitution: true)
			 
			   
		}
	     }
	}
}
		

		
		        

		

					    

			 



  
	
