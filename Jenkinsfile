pipeline
{
stages
{
stage('checkoutfromscm') {
    steps{
    git 'https://github.com/dj19091999/pipeline_project.git'
    }
}
stage('build') {
    steps{
   bat label: '', script: '''cd
cd C:\\dheerajcode\\jenkinproject
"C:\\Program Files\\Git\\bin\\git.exe" log -1
FOR /F "tokens=*" %%a in (\'"C:\\Program Files\\Git\\bin\\git.exe" log -1\') do SET check=%%a
echo %check%
if %check% == dk (cd) else (dir)
copy C:\\WINDOWS\\system32\\config\\systemprofile\\AppData\\Local\\Jenkins.jenkins\\workspace\\jen_pro\\hello.c C:\\Users\\user
cd C:\\Users\\user
dir
dir hello*.c
C:\\Dev-Cpp\\MinGW64\\bin\\gcc -o dheeraj hello.c
dheeraj'''
    }
}
}
}
