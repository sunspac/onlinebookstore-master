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
                      echo " build successfully"  
                      sh "docker build -t bookstore:latest ."
              	    }  
         	    } 
        }
}
