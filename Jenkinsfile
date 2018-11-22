node{
stage('Git checkout')
{
  git 'https://github.com/rohitgarde/RohitsJenkins.git'
}
stage('Make Directory')
{
bat '''set a=c:\\Rohit\\Rohit_jenkins_%BUILD_NUMBER%_%BUILD_TIMESTAMP%
mkdir %a%
cd %a%'''

}
stage('Clone Repos')
{
git  'https://github.com/rohitgarde/RohitsJenkins.git'
}
}
