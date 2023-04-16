pipeline{
	agent{
		dockerfile{
			label 'agent-aws'
		}
	}
	stages{
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
