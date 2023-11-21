pipeline{
	agent{
		node{
			label 'built-in'
		}
	}
	parameters{
		string(name:'PERSON', defaultValue:'Mr.Jenkins', description:'Enter your name: ')
		string(name:"ENVIRONMENT",defaultValue:"",description:"Enter your environment")
	}
	stages{
		stage("BUILD"){
			steps{
				echo "hi, your job run successfully :) "
				echo "Person name is: $params.PERSON" 
				echo "Your environment is $ENVIRONMENT"
			}
		}
	}
}
