Azure app have 4 type of app service :-

 - Web apps = it is use for backend (nodejs)
 - static app = it is for static code like reactjs
 - web app + database = it is for azure database (cosmosdb)
 - word-press on app service = it is for azure wordpress
 
 # Create web app by azure devops :-
 ## steps:-
 1. before run create web app manually
 2. create organization :- (org-CI-CD-mern-app)
       policy->security policies (for make public project (it is benificial to run unlimited free job)
 3. Create Project :- (	project-CI-CD-mern-app)
      create self hosted agent to run job :-
mkdir agent ; cd agent
wget https://vstsagentpackage.azureedge.net/agent/3.227.2/vstsagent-linux-x64-3.227.2.tar.gz
tar zxvf vsts-agent-linux-x64-3.227.2.tar.gz
./config.sh
https://dev.azure.com/org-CI-CD-mern-app7xduhef6jimdzhuirgmifpgfznut6ubfb6ueepwvjzzqtemzquma
./run.sh
4. Create pipeline :-
	pipeline->choose repo platform(git hub) -> chosse repo -> choose base -> start build
5. write "azure-pipeine.yml" file :- for deploy web app with enviourmental variable
when these steps are complete, your web app ready with backend.

# Create static app with azure devops
1. create static app manually :- choose source->other when you create static app 
 
