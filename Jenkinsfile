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
	
	stage('Slack Notification')
	{
		slackSend baseUrl: 'https://hooks.slack.com/services/', 
		channel: '#devopstraining', 
		color: 'good', 
		message: 'welcome to slack_jenkins', 
		tokenCredentialId: 'slack_demo'
	}


}
