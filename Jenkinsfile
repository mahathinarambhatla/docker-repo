pipeline 
{
    agent any
    
    stages 
	{
       stage('Docker Image Build and Push To Nexus')
        {
            when 
            {
                expression { return fileExists('Dockerfile')}
		    }
           steps
            {
	         sh 'docker build -f "Dockerfile" -t trial:1.0  .'  
                 withDockerRegistry(credentialsId: 'b9ba9580-ebea-417d-b0d3-17857027692b', url: 'http://35.231.84.239:8082') 
                     {
			 sh '''
			 whoami
			 docker tag "trial1.0" "docker-trial/trial" 
			 docker push  "docker-trial/trial" 
			'''
                     }                  
		    }
        }
    }

}
