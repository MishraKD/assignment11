pipeline {
	
	environment {
    GIT_URL="https://github.com/MishraKD/assignment11.git"
   
}
	
agent any	
	stages{
            
stage('DeployToProduction') {
	
             steps {
		     sh "ssh -tt -i '/var/jenkins_home/workspace/deployKubeApp/git.pem'  git@172.31.0.110"
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
		
		        

		

					    

			 



  
	
