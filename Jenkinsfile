pipeline {
	
	environment {
    GIT_URL="https://github.com/MishraKD/assignment11.git"
   
}
	
agent any	
	stages{
            
stage('DeployToProduction') {
	
             steps {
		     sh "ssh -i "/var/jenkins_home/workspace/deployKubeApp/git.pem"  git@52.214.113.246"
                    script{
                        try{
				
			    sh  "pwd"	
                         
                        }catch(error){
                           
                        }
                    }
		     
		
	     
	}
}
}
}
		
		        

		

					    

			 



  
	
