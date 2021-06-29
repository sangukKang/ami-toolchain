node {
  stage('Git clone') {
    def scmUrl = scm.getUserRemoteConfigs()[0].getUrl()
    git(url: "${scmUrl}", branch: "${branch}", credentialsId: 'github-sanguk', changelog: true)
  }
  dir ("packer/build_${OS_Type}") { 
    stage ('packer') {
      sh '''
      pwd
      /opt/packer/packer build ./${Target_Image}-ami.json
      '''
    }
  }
}
parameters {
  string(name: 'branch', defaultValue: 'master', description: '디플로이할 대상 브랜치를 입력하세요.')
  choice(name: 'OS_Type', choices: ['awslinux2', 'ubuntu'], description: 'OS를 선택하세요.')
  choice(name: 'Target_Image', choices: ['gitlab', 'jenkins', 'sonarqube', 'frontend'], description: 'AMI를 만들 대상을 선택하세요.')
}
