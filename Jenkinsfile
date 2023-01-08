node {

	stage('SCM Checkout')
	{

		git 'https://github.com/dhananjayksingh/testproject'
		
	}
	
	
	stage('Compile-Package')
	{
		def mvnHome=tool name: 'maven3', type: 'maven'
		sh "${mvnHome}/bin/mvn package"
		
		
	}
	
	stage('Email Notification')
	{
	
		mail bcc: '', body: 'job completed', cc: '', from: '', replyTo: '', subject: 'Jenkins Task', to: 'kdhananjay95@gmail.com'
		
	}

}
