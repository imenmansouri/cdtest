pipeline {
    agent any 
        stages {
            
            stage('Build'){
            steps{
                script{
                    sh "ansible-playbook -vvvv Ansible/build.yml -i Ansible/inventory/host.yml "                    
                    }            
                }
            }
 stage('Docker'){
            steps{
                script{
		    
                    sh "ansible-playbook -vvvv Ansible/docker.yml -i Ansible/inventory/host.yml"
                    }
                }
            }
stage('Docker login') {

            steps {
                   sh 'echo "login Docker ...."'
                   sh "docker login -u imenmansouri -p 09846690++"
                               }  
			}
stage('docker registry')
 {
 steps{
 script{
 sh " ansible-playbook  -vvvv Ansible/docker-registry.yml -i Ansible/hosts.yml "
 }
 }
 }
        }
}
