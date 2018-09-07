node 
{
def maven_home
stage ("checkout the source code")
{
git 'https://github.com/jogeswar18/course.git'
maven_home = tool 'Maven3.5'
}
stage ("build the artifact")
{
sh "'${maven_home}/bin/mvn' package"
}
  stage ("Deploying artifact")
  {
   sh  "scp -i /home/test/test.pem /var/lib/jenkins/workspace/pipeline_job/target/course.war test@13.232.208.231:/home/test/apache-tomcat-9.0.10/webapps"
  }
}
