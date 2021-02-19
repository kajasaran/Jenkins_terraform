Pipeline {

node () {

	stage ('terraform-jenkins - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/kajasaran/Jenkins_terraform.git']]]) 
	}
	stage ('terraform-jenkins - Build') {
 			// Shell build step
sh """
# cd in the cloned repo and pulling changes
cd ~/Documents/devops/Jenkins_terraform

git pull https://github.com/kajasaran/Jenkins_terraform.git

# Starting terraform
ls
/usr/local/bin/docker ps
/usr/local/bin/terraform apply -auto-approve
 """ 
	}
}
}
