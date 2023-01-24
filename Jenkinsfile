pipeline{

agent {label 'dev'}
triggers {
  pollSCM '* * * * *'
}

stages{
stage('scm') {
steps{
checkout scmGit(branches: [[name: '*/feat01']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Preethi9296/mavenrepo.git']])
}
}
stage('bulid') {
steps{
sh 'mvn package'
}
}
  
}
}
