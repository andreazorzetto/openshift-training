node('maven') {

stage 'build'
  openshiftBuild(buildConfig: 'docker-caddy', showBuildLogs: 'true')

stage 'deploy'
  openshiftDeploy(deploymentConfig: 'docker-caddy')
  openshiftScale(deploymentConfig: 'docker-caddy',replicaCount: '2')

}
