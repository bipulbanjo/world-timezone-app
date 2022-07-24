pipeline{
	agent any
		stages{
			stage('Build Application'){
				steps{
					bat 'mvn clean install'
					}
				}
			stage('Munit Test Application'){
				steps{
					bat 'mvn test'
					}
				}
			stage('Deploy Application'){
				steps{
					bat 'mvn package deploy -DmuleDeploy'
					}
				}
			stage('Perform Regression Testing'){
				steps{
					bat 'C:\\Users\\Vishal\\AppData\\Roaming\\npm newman run E:\\TestSuite\\worldtimezone-test-collection.postman_collection.json -r htmlextra --reporter-htmlextra-export E:\\TestSuite --reporter-htmlextra-darkTheme'
					}
				}
			}
		}
					 