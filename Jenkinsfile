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
 
}
