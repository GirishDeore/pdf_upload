
pipeline {
    agent any
	tools{
maven "Maven 3.6.3"} 
    stages {
 /*       stage ('git checkout') {
            steps {
               git credentialsId: 'github',url: 'https://github.com/GirishDeore/pdf_upload.git'
            }
        }
         stage ('Build') {
            steps {
              sh "mvn --version"
              sh "mvn clean install"
            }
        }*/
        stage ('run') {
            steps {
               sshagent(['ec2']) {
 	//	                sh 'scp -v -o StrictHostKeyChecking=no  -i /home/sunbeam/Downloads/girish_key_pairpem.pem target/*.jar ubuntu@13.233.246.111:/home/ubuntu'
sh "ssh -v -o StrictHostKeyChecking=no  -i /home/sunbeam/Downloads/girish_key_pairpem.pem ubuntu@13.233.246.111 './start.sh'"

		}
                 
        
            }
        }
        }
    }
