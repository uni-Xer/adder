pipeline{
	agent{
		docker{
			label 'inbound'
			image 'python:3'
		}
	}
	stages{
		stage('Compile'){
			steps{
				sh 'python3 -m compileall adder.py'
			}
		}
		stage('Run'){
			steps{
				sh 'python3 adder.py 3 5'
			}
		}
		stage('Unit Test'){
			steps{
				sh 'python3 -m unittest adder.py'
			}
		}
	}
}
