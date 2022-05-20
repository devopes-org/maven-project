pipeline
{
agent any
stages
{
stage('scm checkout')
{steps { git branch: 'master', url: 'https://github.com/devopes-org/maven-project.git' }}

stage('build the code')
{ steps {withMaven(jdk: 'JAVA_HOME', maven: 'MAVEN_HOME')
 {sh 'mvn package'}
        } }
 
 stage('deploy to dev')
    {
    steps
    {
     {sh 'scp -o  StrictHostKeyChecking=no *target/*.war 3.69.53.251:/usr/share/tomcat/webapps'}
    }
hi
