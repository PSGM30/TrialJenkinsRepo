pipeline 
{
    agent none
    stages 
	{
        stage('Test on Development Environ')
		{
           	agent any
            	steps 
			{
                	sh 'pip install -r requirements.txt'
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
