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
      stage("deploy"){
        steps{
           deploy adapters: [tomcat8(credentialsId: 'deployeruser', path: '', url: 'http://3.16.206.179:8080/')], contextPath: null, war: '**/*.war'
        }
      }
   }
}
