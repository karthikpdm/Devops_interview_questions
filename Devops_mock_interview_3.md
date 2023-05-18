- Mock interview video - https://youtu.be/IrIF9IjOwgs
- Mock interview Answers - 


GIT
---------------------------------------------------------------------------------------------------------------------------------
1. What is git-cherry-pick? why we use it?
ans:herry picking is the act of picking a commit from a branch and applying it to another.
3. Let’s say you’re working on new feature in some branch, now your manager says stop working on that and change few other things on old code. Here after changing the old code, I need to work on new code, so I need to place my new changes some place How would handle this scenario? use git stash
4. What is a conflict in git?
5. command to list all branches in a repo? git branch -a



Maven
--------------------------------------------------------------------------------------------------------------------------
5. .m2 is local repository for maven, now I don’t want to use .m2 folder as my local repository I want to use some other folder as my local, is it possible in maven? If yes, how would you do that?
m2 folder is the default folder used by maven to store its: settings.xml file which specifies properties, like the central repository to download your dependencies, the location of the so-called localRepository. by default, the localRepository in which maven stores all the dependencies your project might need to run.

```
mvn install -Dmaven.repo.local=/alternate/repo/location 
```
6. maven follows convention over configuration that means it assumes code should be there under src/main/java, test cases under src/tests and many more.Here my requirement is I don’t want to follow that conventions I need to use different folder structure is that possible in maven?
```
mvn help:effective-pom -Doutput=pom_eff.xml
```
7. What are dependency and plugin in maven? Give one example for each?
A Maven plugin is an addition you can utilize to create your artifact (maven-jar-plugin is used to make a jar out of your compiled classes and resources). A library required by the application you are building during compilation, test, or runtime is known as a dependency.

9. What are 3 build life cycles in maven?
There are three built-in build lifecycles.
default: handles project build and deployment.
clean: handles project cleaning.
site: handles the creation of project site documentation.

Maven Build Phases
Maven build lifecycle goes through a set of stages, they are called build phases. For example, the default lifecycle is made up of the following phases.

validate
compile
test
package
verify
install
deploy
The build phases are executed sequentially. When we run a maven build command, we specify the phase to be executed. Any maven build phases that come before the specified phase is also executed. For example, if we run mvn package then it will execute validate, compile, test, and package phases of the project.

Maven Build Goals
A build phase is made up of a set of goals. Maven goals represent a specific task that contributes to the building and managing of a project. Sometimes, a maven goal is not bound to a build phase. We can execute these goals through the command line. The syntax to execute a goal 

11. In Which tag we will mention output artifact type( like jar, war or any other)?

Unix and Shell scripting 
---------------------------------------------------------------------------------------------------------------------
10. In a file I have ip addresses , I want list unique ip addresses with number of times its present in file?
```
grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" logfile | sort | uniq -c | sort -nr
```
11. What is exit status in UNIX?
Exit status is an integer number. 0 exit status means the command was successful without any errors. A non-zero (1-255 values) exit status means command was a failure.

13. Lets say I have shell script name magic.sh when I execute. It gives “This is from magic.sh”, so now if I change file name to magic-test.sh I should get “This is from magic-test.sh” basically as name of file chages my output should also change?
echo $0

15. What is shebang ? Why it is used?
It is used to specify the interpreter with which the given script will be run by default.
The most common use of the Shebang is to specify the correct shell to use for a shell script. If a Shebang is not specified, the system uses the default interpreter belonging to the current shell

Jenkins 
--------------------------------------------------------------------------------------------------------
14. How to Downgrade plugins in Jenkins?
To manually downgrade the Jenkins Artifactory plugin:
Shut down Jenkins.
Delete the artifactory.jpi file and the artifactory folder from ${user_home}/.jenkins/plugins.
Place the older artifactory.hpi file.
Start Jenkins. Release Fast Or Die. Products. Artifactory.
16. Have you worked on Jenkinsfile? Can we use different nodes for each stage?yes
17. Can you list few ways by which we can trigger our build in Jenkins?
   (a) Trigger builds remotely :
If you want to trigger your project built from anywhere anytime then you should select Trigger builds remotely option from the build triggers.
You’ll need to provide an authorization token in the form of a string so that only those who know it would be able to remotely trigger this project’s builds. This provides the predefined URL to invoke this trigger remotely.

   (b) Build after other projects are built
If your project depends on another project build then you should select Build after other projects are built option from the build triggers.

In this, you must specify the project(Job) names in the Projects to watch field section and select one of the following options:
1. Trigger only if the build is stable
Note: A build is stable if it was built successfully and no publisher reports it as unstable
2. Trigger even if the build is unstable
Note: A build is unstable if it was built successfully and one or more publishers report it unstable
3. Trigger even if the build fails
    
    (C)Build periodically:
If you want to schedule your project build periodically then you should select the Build periodically option from the build triggers.
You must specify the periodical duration of the project build in the scheduler field section
    
     (D)GitHub webhook trigger for GITScm polling:
A webhook is an HTTP callback, an HTTP POST that occurs when something happens through a simple event-notification via HTTP POST.

GitHub webhooks in Jenkins are used to trigger the build whenever a developer commits something to the branch.
note:et’s see how to add build a webhook in GitHub and then add this webhook in Jenkins.

Go to your project repository.
Go to “settings” in the right corner.
Click on “webhooks.”
Click “Add webhooks.”
Write the Payload URL as

     (E) Poll SCM:
Poll SCM periodically polls the SCM to check whether changes were made (i.e. new commits) and builds the project if new commits were pushed since the last build.

You must schedule the polling duration in the scheduler field. Like we explained above in the Build periodically section. You can see the Build periodically section to know how to schedule.
19.  What is the difference between Build Periodically and Poll SCM? 

AWS
-------------------------------------------------------------------------------------------------------------
17. What are roles and policies in AWS IAM?
18. Lets say I have 50 users , for all 50 users I need to provide same privileges how do it? 
19. I want to give programmatic access means They can access AWS services via api’s  But should not be access AWS web console
20. As AMI is region specific I want create Machine with AMI which there in other Region is that possible?
21. Why we need security groups? By default what is outbound rules?
22. What is VPC? Give a brief about VPC?
23. Have you worked on Load balancers? If Yes, tell which load balancers you have used?
24. Lets say I have created auto scaling rule when ever Load goes more than 60% create a new instance Currently I have 3 machines, 1st machine load  is 62% , 2nd machine 30% and 3rd also 30%.  Now will auto scale rule creates new machine ?

Ansible
-----------------------------------------------------------------------------------------------------------------------
25. What is the best method to make your ansible YAML files reusable?
26. What is ansible vault and ansible tower?
27. Lets say I have playbook need to be run with Root user how would you do this?
28. Difference between copy and fetch module?
29. What is Ansible Galaxy?
What is an Ansible galaxy?
a)Ansible Galaxy is essentially a large public repository of Ansible roles. Roles ship with READMEs detailing the role's use and available variables. Galaxy contains a large number of roles that are constantly evolving and increasing. Galaxy can use git to add other role sources, such as GitHub
b)Galaxy provides pre-packaged units of work known to Ansible as roles and collections. Content from roles and collections can be referenced in Ansible PlayBooks and immediately put to work. You'll find content for provisioning infrastructure, deploying applications, and all of the tasks you do everyday.
c)Ansible is an open-source configuration management tool while Ansible Galaxy is a repository for Ansible roles.
d)Ansible can communicate with configured clients from the command line by using ansible command. It also allows you to automate configuration by using ansible-playbook command. To create the base directory structure, you can use a tool bundled with Ansible which is known as ansible-galaxy.

Docker
------------------------------------------------------------------------------------------------------------------------------
29. Lets say I have 1 GB file that has to be sent to docker daemon, as its 1GB it will take muchtime and network too. By which option while building dockerfile we can send the fileIn better manner?
30. What is the difference between ADD and COPY docker instructions in Dockerfile?
31. Command to remove to stopped and running Containers? docker rm $(ps-aq)
32. Inside the container I did many changes like  Creating, modifying and deleting file but I Wanted to check which files has been changed And what action has been taken what is the  Command we need to use ?


Kubernetes
--------------------------------------------------------------------------------------------------------------------------------------
33. List objects you know in kubernetes?Give a brief about each object?
34. Command to list pods and deployments

