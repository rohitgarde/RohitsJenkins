node{
stage('Git checkout')
{
  git 'https://github.com/rohitgarde/RohitsJenkins.git'
}
stage('Make Directory')
{
  a=c:\Rohit\Rohit_jenkins_%BUILD_NUMBER%_%BUILD_TIMESTAMP%
mkdir %a%
}
stage('Clone Repos')
{
"C:\Program Files\Git\cmd\git.exe" clone https://github.com/rohitgarde/RohitsJenkins.git
}
}
