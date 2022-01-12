pipeline
{
agent any
stages
{
stage('scm checkout')
{steps { git branch: 'master', url: 'https://github.com/devopes-org/maven-project.git' }}

stage('build the code')
{ steps {withMaven(globalMavenSettingsConfig: 'null', jdk: 'JAVA_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: 'null')
 {sh 'mvn package'}
 } 

}
}
}


