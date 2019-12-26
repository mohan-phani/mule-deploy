pipeline
{
	agent any
	stages
	{
		stage('Build Application'){
			steps{
				bat 'mvn clean install -DskipTests'
			}
		}
		stage('Munit Test Application'){
			steps{
				bat 'mvn clean verify'
			}
		}
		stage('Deploy Application To Mulesoft'){
			steps{
				bat 'mvn package deploy -DmuleDeploy'
			}
		}
	}
}