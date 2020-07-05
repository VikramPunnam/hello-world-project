pipeline {
  agent any
  environment{
    PATH = "/opt/apache-maven-3.6.3/bin:$PATH" 
  }
  stages{
      stage("git"){
        steps{
	  git 'https://github.com/vikramvicky61/hello-world-project.git'
	}
      }
      stage("build"){
        steps{
          sh "mvn clean install"
        }
      }
    }
}
