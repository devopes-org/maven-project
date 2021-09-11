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

}

}                    






