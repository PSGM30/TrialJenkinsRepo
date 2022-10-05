pipeline 
{
    agent none
    stages 
	{
        stage('Test on Development Environment')
		{
           	agent any
            	steps 
			{
			echo 'This is Build part'
			
			sh 'python app.py'
				
			echo 'This is Test part'
                	
                	sh 'python test.py'
            		}
            	post 
			{
                	always 
				{
                    		junit 'test-reports/*.xml'
                		}
            		}
        	}
        
    	}
}
