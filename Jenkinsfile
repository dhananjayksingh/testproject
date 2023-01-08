node {

	stage('SCM Checkout')
	{
		git 'https://github.com/dhananjayksingh/testproject'
		
	}
	
	
	stage('Compile-Package')
	{
		gsh 'mvn package'
		
	}

}
