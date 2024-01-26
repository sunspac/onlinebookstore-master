pipeline {  
    agent any  
        stages {  
       	    stage("build") {  
           	    steps {  
                      echo " build successfully"  
                      sh "mvn clean package"
              	    }  
         	    } 
            stage("build docker Image") {  
           	    steps {  
                      sh "docker build -t sunspace:1 ."
                      sh "docker tag sunspace:1 decawsdevops/sunspace:3"
                      echo " build successfully"  
              	    }  
         	    } 
            stage("publish to registry") {
                steps {
                    withDockerRegistry(credentialsId: 'dockerhub', url: 'https://hub.docker.com/repositories/decawsdevops') {
                           sh "docker push decawsdevops/sunspace:3"
                    }
                }

            }
        }
}
