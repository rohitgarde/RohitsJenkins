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
 

}
stage('Clone Repos')
{

    def a=env.BUILD_NUMBER+"_"+env.BUILD_TIMESTAMP
  def b="c:\\Rohit\\Build_" + a 
  echo "${b}"
  checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir:b]], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/rohitgarde/RohitsJenkins.git']]])
}
}
