pipeline {
	
	environment {
    GIT_URL="https://github.com/MishraKD/assin11.git"
    DEPLOY_DEL="kubectl delete deployment nginx-deployment"
		
	}
	
agent any	
	stages{
            
stage('DeployToProduction') {
	
             steps {
		     script {
                  def nglabels = label 'nginx'
                if(nglabels){
                 
                       // sh 'kubectl delete deployment nginx-deployment'
                      // podTemplate pod :"${env.DEPLOY_DEL}"
                     nginx :"${env.DEPLOY_DEL}"
                      git url: "${GIT_URL}"
		     
		    // git url: "${GIT_URL}"
		  
            
             kubernetesDeploy(
		     
		    
                    credentialsType: 'KubeConfig',
                    //kubeconfigId: 'kubeconfig',
                    kubeConfig: [path: '/var/jenkins_home/workspace/.kube/config'],
                    configs: 'deploymentfile.yml',

                    enableConfigSubstitution: true   
             )
			 }
			     else{
			     echo 'deployment failed'
				     

            }
		}
	     }
}
		

		
		        

		
		stage('performance Testing') {
		        steps {
				
				//sh '/var/jenkins_home/soapui/SoapUI-5.2.1/bin/testrunner.sh -s"TestSuite 1" -c"TestCase 1" -r /var/jenkins_home/workspace/KuberTesting2_SoapUi/REST-Project-1-soapui-project.xml'
				//bat 'c:/jmeter/bin/jmeter.bat -n -t c:/jmeter/extras/Test.jmx -l test.jtl'
				///var/jenkins_home/JMeter/jakarta-jmeter-2.5/bin/Smarthire.jmx 
				sh 'pwd'
				sh '/var/jenkins_home/JMeter/jakarta-jmeter-2.5/bin/jmeter.sh -n -t  /var/jenkins_home/workspace/deployKubeApp/stock-sim.jmx -l test.jtl'          // PERFORMANCE_PATH="/var/jenkins_home/JMeter/jakarta-jmeter-2.5/bin"
			//microservice/performance-scripts	
	            //cd '$PERFORMANCE_PATH'
				
	                             // sh 'jmeter.sh -n -t $WORKSPACE/microservice/performance-scripts/$JMX.jmx -l $WORKSPACE/$JMX.jtl'
		                       
		                    
		                
		            }
		    }
				stage('soapui') {
	        steps {
			echo 'soapui'
			
	               //sh '/var/jenkins_home/SoapUI-5.2.1/bin/testrunner.sh -s"Sample REST Project 1" -c"TestCase 1" -r /var/jenkins_home/workspace/deployKubeApp/REST-Project-1-soapui-project.xml' 

			
		}
				}
	    

					    





  }
}
