pipeline{
	agent{
		node{
			label 'built-in'
		}
	}
	parameters{
		string(name:'PERSON', defaultValue:'Mr.Jenkins', description:'Enter your name: ')
	}
	stages{
		stage("BUILD"){
			steps{
				echo "hi, your job run successfully :) "
				echo "Person name is: $params.PERSON" 
			}
		}
	}
}
