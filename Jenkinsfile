/*pipeline {
    agent any 
tools{
maven "Maven 3.6.3"} 
    stages {
        stage ('Build') {
            steps {
               sh "mvn --version"
		sh "mvn clean install"
             }
           }
         }
      }
*/
pipeline {
    agent any
	tools{
maven "Maven 3.6.3"} 
    stages {
        stage ('git checkout') {
            steps {
               git credentialsId: 'github',url: 'https://github.com/GirishDeore/pdf_upload.git'
            }
        }
       /*  stage ('Build') {
            steps {
              sh "mvn --version"
              sh "mvn clean install"
            }
        }
	
        stage ('run') {
            steps {
               sshagent(['tomcat']) {
 		  sh 'scp -o StrictHostKeyChecking=no target/*.jar ubuntu@13.233.229.40:~/'
		   //        sh 'ssh -o StrictHostKeyChecking=no -l cloudbees 192.168.1.106 uname -a'

		}
            }
        }*/
	     stage ('run with normal') {
            steps {
               
 		  sh 'scp -i /home/sunbeam/Downloads/girish_key_pairpem.pem /home/sunbeam/GitHub/pdf_upload/target/pdf_file_upload-0.0.1-SNAPSHOT.jar ubuntu@13.233.229.40:~/'
		   //        sh 'ssh -o StrictHostKeyChecking=no -l cloudbees 192.168.1.106 uname -a'
            }
        }
	    
	    
        }
    }
