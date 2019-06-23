pipeline{
 	agent any
		stages{
			stage('one'){
				steps{
					echo 'hi,this is sandeep from cloudbuddies'
				}
			}

			stage('two'){
				steps{

					input('do you want to proceed')
					}
				}
			stage('three'){
				when{
					not{
						branch "master"
						}
					}
				steps
					{
						echo "hello"
 					}
		}
	stage('four') {
			parallel {
					stage('unit test'){
						steps {
							echo "runnug the unit test"
						}
					}
					
			
			stage('integration test'){
					agent{
						docker{
							reuseNode false
							image 'ubuntu'
								}
						}
					steps{
						echo 'running integration testing'
							}
			}
	}
}
}
}
}
