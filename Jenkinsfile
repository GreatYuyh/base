node  {

  stage ('Checkout') {
   git branch: '${gitBranch}', credentialsId: 'git-ssdc-kube', url: '${gitUrl}'
  }

  withMaven(maven: 'M3') {

      stage('maven package') {
       sh "mvn clean package"
      }

  }

}
