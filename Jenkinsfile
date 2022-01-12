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
    sh scp -o  StrictHostKeyChecking=no **/*.war 192.168.227.206:/usr/share/tomcat/webapps
    }
    }
