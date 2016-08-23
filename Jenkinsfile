node {
  stage "Cleanup Docker"
    EXIT_STATUS=0
    sh "docker ps -a | grep 'hours ago' | grep -v 'ideaflow/jenkins' | grep -v mysql | awk '{print \$1}' | xargs --no-run-if-empty docker rm -f || EXIT_STATUS=$?"
    sh "docker images | grep hour | grep -v 'ideaflow/jenkins' | grep -v 'mysql' | grep -v 'node' | awk '{print \$3}' | xargs docker rmi -f || EXIT_STATUS=$?"
    exit $EXIT_STATUS
}
