node{
  environment{
  build=env.BUILD_NUMBER
    ts=env.BUILD_TIMESTAMP
  
  }
stage('Git checkout')
{
  git 'https://github.com/rohitgarde/RohitsJenkins.git'
}
stage('Make Directory')
{
bat '''set a=c:\\Rohit\\Rohit_jenkins_%BUILD_NUMBER%_%BUILD_TIMESTAMP%
mkdir %a%
cd %a%'''
  echo 'hello'
  echo env.BUILD_NUMBER+env.BUILD_TIMESTAMP
  echo env.BUILD_NUMBER
   def a=env.BUILD_NUMBER+env.BUILD_TIMESTAMP
  echo "${a}"

}
stage('Clone Repos')
{
  bat '''set a=c:\\Rohit\\Rohit_jenkins_%BUILD_NUMBER%_%BUILD_TIMESTAMP%

cd %a%'''
  
  checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir:'c:\\Rohit\\Rohit_jenkins_env.BUILD_NUMBER_env.BUILD_TIMESTAMP']], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/rohitgarde/RohitsJenkins.git']]])
}
}
