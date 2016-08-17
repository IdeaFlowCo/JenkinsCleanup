node { 
	stage "Cleanup Docker"
		sh "docker ps -a | grep "days ago" | grep -v jenkins | grep -v mysql | awk '{print \$1}' | xargs --no-run-if-empty docker rm"
		sh "docker images | grep days | grep -v "jenkins" | grep -v "mysql" | grep -v "node" | awk '{print \$3}' | xargs docker rmi"
}
