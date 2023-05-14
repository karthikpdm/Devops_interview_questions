- Mock interview video - https://youtu.be/i7YJesoeWFI
- Mock interview Answers - https://youtu.be/5w8qVukxXXY 

GIT
---------------------------------------------------------------------------------------------------------------------------------
1. Why we need git? What makes git unique from other tools like SVN?
2. Let's say i have maven repo cloned on to my local, did some changes and i have build the code now target folder will be generated. So now when i do git operations like git add, git commit or any other git operations target folder should not be considered, how would you achieve the same?
ans : use .gitignore
4. difference between git pull and git fetch?
5. How to clone specific branch in git?
Ans : git clone -b <baranch_name> --single-branch url
after we list the branches using the git branch -a it will list that particular branch only

Maven
--------------------------------------------------------------------------------------------------------------------------
5. when i issue mvn install what all things happen in background?
![image](https://github.com/karthikpdm/Devops_interview_questions/assets/108477836/75ca0977-2e7b-484d-9cb9-805d98950a80)

7. what are the settings you need to do before running mvn deploy?
Ans : with respect where we are uploading our artifacts like jfrog,nexas etc
we need to give the url of the reposiory and username and password of that remote repository.
9. why maven takes much time for 1st execution and from 2nd execution it will take less time?
Ans:so for the first time if we clone the repo it will store it in the .m2 folder so if we clone for the 2nd time it first check
in the local repo and if it already exist then it will skip the cloaning, other then that it will clone.

Unix and Shell Scripting 
--------------------------------------------------------------------------------------------------------
8. How to get present working folder?
Ans : basename "$pwd"
10. How to copy files from local windows machine to cloud based Linux machine?
11. A shell script named test.sh can accept 4 parameters i.e, a,b,c,d. the parameters wont be supplied in order always and number of parameters might also vary( only 2 parameters user might supply sometimes), how to identify position of letter c?

Ansible
---------------------------------------------------------------------------------------------------------------------
11. Why we need ad-hoc ansible commands, scenario where you have used ansible ad-hoc command?
12. When i need detailed logs on executing ansible playbook what option i need to use?
13. what is ansible.cfg file?
14. what are the modules have you worked on? which module will you use for getting the file from node to master?
15. Lets say i have a playbook which has 5 tasks in playbook, first 2 tasks should run on local machine and other 3 tasks should run on node?
Ans : 1) using the single play and the multiple play so in the multiple play we can mention the multiple hosts so in the first host we can run the 2 tasks amd
in the other host we can run the other 3 tasks.
2) usin the when condition also we can do this purpose.


Jenkins
-----------------------------------------------------------------------------------------------------------------------
16. How to save only last 5 builds of jenkins job?
17. Have you worked on Jenknsfile? can we use docker container as a node in Jenkinsfile? Who will handle docker container creation and deletion? If i am building a maven project always docker container is fresh instance it will try to download dependency from repository, what measures you will take to reduce build time?
18. Why we need multi branch pipeline?
19. If you forget Jenkins password, how would you login back?

Docker
------------------------------------------------------------------------------------------------------------------------------
20. Any 3 best practices of docker?
21. Difference between docker stop and docker kill?
22. Command to list conatiners which state is exited?
23. command to clean-up docker host ( deleting stopped conatiners, dangling images and unused networks)?
24. What version of docker you have used? Specific reason to use that particular version?
25. Can we have multiple CMD in Dockerfile?
26. Have you worked on docker swarm and docker compose?

Kubernetes
--------------------------------------------------------------------------------------------------------------------------------------
27. Can we have multiple conatiners in a pod? Can we have similar conatiners in a pod? Lets say i have 4 conatiners, one of them has failed how would you check which container has failed?
28. What is liveness and readiness probe? Why we need them?
29. Have you worked on kubernetes monitoring? Which tools you have used?
30. Can we deploy a pod on particular node?
