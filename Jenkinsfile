pipeline {
	agent any
	stages {
		stage('Kubernetes deploy') {
			steps {
				kubernetesDeploy config: "deployment.yaml" kubeconfigId: 'best-practice'
				sh "kubectl get all"
			}
		}
	}
}
