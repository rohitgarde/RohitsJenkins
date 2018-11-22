node{
  environment{
  build=env.BUILD_NUMBER
    ts=env.BUILD_TIMESTAMP
  
  }
stage('Git checkout')
{
  git 'https://github.com/rohitgarde/RohitsJenkins.git'
}

stage('Clone Repos')
{

    def a=env.BUILD_NUMBER+"_"+env.BUILD_TIMESTAMP
  def b="c:\\Rohit\\Build_" + a 
  echo "${b}"
  checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir:b]], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/rohitgarde/RohitsJenkins.git']]])
}
}
