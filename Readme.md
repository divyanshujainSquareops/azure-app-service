Azure app have 4 type of app service :-

<img width="956" alt="image" src="https://github.com/divyanshujainSquareops/azure-app-service/assets/148210383/1fd8763d-999a-4254-8dba-2c09514bb75c">


 - Web apps = it is use for backend (nodejs)
 - static app = it is for static code like reactjs
 - web app + database = it is for azure database (cosmosdb)
 - word-press on app service = it is for azure wordpress
 
 # Create web app by azure devops :-
 ## steps:-
 1. before run create web app manually
 2. create organization :- (org-CI-CD-mern-app)
       policy->security policies (for make public project (it is benificial to run unlimited free job)

       <img width="935" alt="image" src="https://github.com/divyanshujainSquareops/azure-app-service/assets/148210383/14ff84e2-bf06-4cd1-a6b1-bcb41fadd570">

    
 4. Create Project :- (	project-CI-CD-mern-app)

    <img width="706" alt="image" src="https://github.com/divyanshujainSquareops/azure-app-service/assets/148210383/a601fb14-66fe-4600-911f-d43d84f93d3d">


    create self hosted agent to run job :-
               mkdir agent ; cd agent
               wget https://vstsagentpackage.azureedge.net/agent/3.227.2/vstsagent-linux-x64-3.227.2.tar.gz
               tar zxvf vsts-agent-linux-x64-3.227.2.tar.gz
               ./config.sh
               https://dev.azure.com/org-CI-CD-mern-app7xduhef6jimdzhuirgmifpgfznut6ubfb6ueepwvjzzqtemzquma
               ./run.sh
6. Create pipeline :-
	pipeline->choose repo platform(git hub) -> chosse repo -> choose base -> start build
7. write "azure-pipeine.yml" file :- for deploy web app with enviourmental variable
when these steps are complete, your web app ready with backend.

# Create static app with azure devops
1. create static app manually :- choose source->other when you create static app 
2. create pipeline and integrate with github/azure repo
3. write yaml file for automation
4. run pipeline and your changes autmatically deploy on azurestatic service
