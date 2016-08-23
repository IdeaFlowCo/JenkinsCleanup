node {
  stage "Cleanup Docker"
    try {
      sh "docker ps -a | grep 'hours ago' | grep -v 'ideaflow/jenkins' | grep -v mysql | awk '{print \$1}' | xargs --no-run-if-empty docker rm -f"
      sh "docker images | grep hour | grep -v 'ideaflow/jenkins' | grep -v 'mysql' | grep -v 'node' | awk '{print \$3}' | xargs docker rmi -f
    }
    catch {
      sh "docker images | grep hour | grep -v 'ideaflow/jenkins' | grep -v 'mysql' | grep -v 'node' | awk '{print \$3}' | xargs docker rmi -f
    }
}
