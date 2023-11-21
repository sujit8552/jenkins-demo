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
	}
}
