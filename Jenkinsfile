node{
  environment{
  
  a='c:\\Rohit\\Rohit_jenkins_BUILD_NUMBER_BUILD_TIMESTAMP'
    echo a
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

}
stage('Clone Repos')
{
  bat '''set a=c:\\Rohit\\Rohit_jenkins_%BUILD_NUMBER%_%BUILD_TIMESTAMP%

cd %a%'''
  
  checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir:'c:\\Rohit\\Rohit_jenkins_BUILD_NUMBER_BUILD_TIMESTAMP']], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/rohitgarde/RohitsJenkins.git']]])
}
}
