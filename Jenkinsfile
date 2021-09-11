pipeline 
{
  agent any
  stages 
  {
      stage('scm checkout')
    {steps { git branch: 'master' , url: 'https://github.com/devopes-org/maven-project'}}


stage ('build the code') 
{steps { withMaven(jdk: 'JAVA_HOME', maven: 'MAVEN_HOME') 
{ sh 'mvn package' }
  
}}
//terraform and ansible stages to automate instance
stage('deploy to dev') 
{
  steps
  {
    sshagent(['tomcat-pipeline'])
    {sh 'scp -o StrictHostKeyChecking=no **/*.war ec2-user@172.31.0.188:/usr/share/tomcat/webapps'}
    }
}


}

                   






