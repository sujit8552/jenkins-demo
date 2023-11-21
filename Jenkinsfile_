pipeline{
	agent{
		node{
			label 'built-in'
			customWorkspace '/home/ec2-user'
		}
	}
	parameters{
		string(name:'PERSON', defaultValue:'Mr.Jenkins', description:'Enter your name: ')
		string(name:"ENVIRONMENT",defaultValue:"DEV",description:"Enter your environment")
		booleanParam(name:'DRUNK',defaultValue:false,description:'Have you drunk water')
		choice(name:'CHOICE',choices:['one','two','three'],description:'Pickone')
		password(name:"PASSWORD",defaultValue:'SECRET',description:'Enter password')
	}
	stages{
		stage("BUILD"){
			steps{
				echo "hi, your job run successfully :) "
				echo "Person name is: $params.PERSON" 
				echo "Your environment is $ENVIRONMENT"
				sh '''
				touch 11.txt
				pwd
    				'''
			}
		}
		stage('ENV VARIABLE'){
			steps{
				echo "The build number is ${env.BUILD_NUMBER}"
				echo "The build id is ${env.BUILD_ID}"
				echo "The build dislplay name is ${env.BUILD_DISPLAY_NAME}"
				echo "The job name is ${env.JOB_NAME}"
				echo "The node name is ${env.NODE_NAME}"
				echo "The node labels is ${env.NODE_LABELS}"
				echo "The build id is ${env.JENKINS_HOME}"
				echo "The workspace is ${env.WORKSPACE}"
			}
		}
	}
}
