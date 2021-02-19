pipeline {
		stage('Cloning Git'){
					steps {
						script{
							sh 'git clone https://github.com/kajasaran/Jenkins_terraform.git' 
						}		
					}
				}

			stage('kube running'){
				steps{
					script {
						sh 'kubectl get services'
					}
				}				
			}
}
