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
                      echo " build successfully"  
              	    }  
         	    } 
        }
}
