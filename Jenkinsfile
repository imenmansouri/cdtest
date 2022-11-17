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
    }
}
