pipeline {
	agent any
	stages {
		stage('Kubernetes deploy') {
			steps {
				kubernetesDeploy config: "deployment.yaml", kubeconfigId: 'best-practice'
				sh "kubectl --kubeconfig=/root/.jenkins/.kube/config rollout restart deployment/wildfly-deployment"
				sh "kubectl get all"
			}
		}
	}
}
