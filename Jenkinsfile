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
   sh  "scp -i  /home/test/test.pem /var/lib/jenkins/workspace/pipeline_job/target/course.war test@13.233.16.70:/home/ec2-user/apache-tomcat-9.0.11/webapps"
  }
}
