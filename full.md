AIM: To understand DevOps: Principles, Practices, and DevOps Engineer Role and Responsibilities.  

FULL THEORY  

---  

AIM: To understand Version Control System, install git and create a GitHub account.  

-----How to install git-----  

Download the latest version of Git and choose the 64/32 bit version. After the file is downloaded, install it in the system.  
https://git-scm.com/downloads (official link)  

If you already have Git installed, you can get the latest development version via Git itself:  
git clone https://github.com/git/git  

-----What is Github and Github account-------  

Understand the basic difference between GIT & GitHub  
Create a github account or login to your existing account  

---  

AIM: To perform various GIT operations  

1. `git config`  

   - Utility: To set your user name and email in the main configuration file.   
   - How to: To check your name and email type in `git config --global user.name` and `git config --global user.email`.  

2. `git init`  

   - Utility: To initialize a Git repository for a new or existing project.  
   - How to: Run `git init` in the root of your project directory.  

3. `git clone`

   - Utility: To copy a Git repository from a remote source, also sets the remote to the original source so that you can pull again.
   - How to: Run `git clone <clone git URL>`.

4. `git status`

   - Utility: To check the status of files you’ve changed in your working directory, i.e., what has changed since your last commit.
   - How to: Run `git status` in your working directory to list all the files that have been changed.

5. `git add`

   - Utility: Adds changes to the stage/index in your working directory.
   - How to: Run `git add .` to stage all changes.

6. `git commit`

   - Utility: Commits your changes and sets them to a new commit object for your remote.
   - How to: Run `git commit -m "sweet little commit message"`.

7. `git push`/`git pull`

   - Utility: Push or pull your changes to/from the remote repository.
   - How to: Run `git pull <remote> <branch>` to pull and `git push <remote> <branch>` to push.

8. `git branch`

   - Utility: Lists out all the branches.
   - How to: Run `git branch` or `git branch -a` to list all the remote branches as well.

9. `git checkout`

   - Utility: Switch to different branches.
   - How to: Run `git checkout <branch>` or `git checkout -b <branch>` to create and switch to a new branch.

10. `git stash`

    - Utility: Save changes that you don’t want to commit immediately.
    - How to: Run `git stash` in your working directory. Use `git stash apply` if you want to bring your saved changes back.

11. `git merge`

    - Utility: Merge two branches you were working on.
    - How to: Switch to the branch you want to merge everything into and run `git merge <branch_you_want_to_merge>`.

12. `git reset`

    - Utility: Reset your index to the latest commit that you want to work on.
    - How to: Run `git reset <mode> <COMMIT>`.

13. `git remote`

    - Utility: To check what remote/source you have or add a new remote.
    - How to: Run `git remote` to check and list. Use `git remote add <remote_url>` to add a new remote.

14. `git log`

    - Utility: To view a log of all the commits in the repository, including commit messages, authors, timestamps, and commit hashes.

15. `git diff`

    - Utility: To view differences between the working directory and the last commit, or between two commits.

16. `git fetch`

    - Utility: To fetch changes from a remote repository without merging them.

17. `git rebase`

    - Utility: To incorporate changes from one branch into another by moving or combining commits.

18. `git tag`

    - Utility: To create, list, delete, or verify tags used for marking specific points in the commit history.

19. `git cherry-pick`

    - Utility: To pick a single commit or a range of commits from another branch and apply them to the current branch.

20. `git remote -v`

    - Utility: To display detailed information about remote repositories, including their URLs, for both fetching and pushing.

21. `git show`

    - Utility: To show information about a specific commit, including the changes introduced in that commit.

22. `git clean`

    - Utility: To remove untracked files from your working directory.

23. `git grep`

    - Utility: To search for a specific string or pattern in the repository's files.

24. `git revert`

    - Utility: To create a new commit that undoes the changes introduced by a previous commit.

25. `git bisect`
    - Utility: To perform a binary search to identify a specific commit where a bug was introduced.

---

AIM: To understand Continuous integration, Jenkins installation

https://www.jenkins.io/download/

---

AIM: To build Java program using Jenkins.

Step 1: Set Up Your Java Project
Step 2: Configure Jenkins
Step 3: Create a Jenkins Job
Step 4: Save and Build
Step 5: View Build Results

CODE:
public class hello{ public static
void main(String[] args)
{ for(int i=1;i<=15;i++)
{
System.out.println("hi Nidhi"+ i );
} } }

Step 6: Adding github Repository URL to jenkins dashboard
Step 7: Execute Windows batch command on jenkins dashboard
javac filename.java
java filename

Step 8: Click and save on jenkins dashboard
Step 9: Upload the java file on your specified githu repository
Step 10: On jenkis dashboard click BUILD NOW
Step 11: The file has been uploaded on console (jenkins dashboard)

---

AIM: To build pipeline using Jenkins.

Step 1: Create a New Pipeline Job

1. Log in to your Jenkins dashboard.
2. Click on "New Item" to create a new job.
3. Enter a name for your pipeline job and select "Pipeline" as the job type.
4. Click "OK" to create the job.

Step 2: Configure Pipeline Definition

1. In the job configuration, scroll down to the "Pipeline" section.
2. In the "Definition" dropdown, select "Pipeline script from SCM" if your pipeline script is in version control (e.g., Git or SVN). Otherwise, choose "Pipeline script."
3. If using "Pipeline script from SCM," provide the SCM details (repository URL, credentials, etc.).
4. If using "Pipeline script," you can directly write your pipeline script in the "Script" text area.

Step 3: Write the Pipeline Script

1. Write your Jenkins pipeline script in Groovy DSL. This script defines the stages and steps of your build, test, and deployment process.
2. Common pipeline stages include checkout, build, test, and deploy. Here's a simple example:

```groovy
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                sh './deploy-script.sh'
            }
        }
    }
}
```

Step 4: Save and Build

1. Save your job configuration.
2. Click on "Build Now" to trigger your first pipeline run.

Step 5: Monitor Pipeline Progress

1. Go to the pipeline job's dashboard to monitor the progress of the pipeline run.
2. Click on a specific build number to see the console output and logs for each stage.

Step 6: Configure Pipeline Triggers (Optional)

1. To automate pipeline runs on code commits or other triggers, configure webhooks or polling schedules.
2. Jenkins can automatically start the pipeline when changes are pushed to your version control system.

Step 7: Notifications (Optional)

1. Configure email notifications or integrate with messaging platforms like Slack to receive alerts on pipeline status.

Example 2:
pipeline {
agent any
stages {
stage('Build') {
steps {
echo 'Hi GeekFLare. Starting to build the App.'
}
}
stage('Test') {
steps {
input 'Do you want to proceed?'
}
}
stage('Deploy') {
parallel {
stage('Deploy start') {
steps {
echo 'Start the deploy...'
}
}
stage('Deploying now') {
agent {
docker {
reuseNode true
image 'nginx'
}
}
steps {
echo 'Docker Created'
}
}
}
}
stage('Prod') {
steps {
echo 'App is prod ready'
}
}
}
}

---

AIM: To understand Docker architecture and container life cycle, install docker, deploy container in docker.

![Docker Architecture](image.png)
![Docker Container Life Cycle](image-1.png)

Docker Installation:
https://docs.docker.com/desktop/install/windows-install/

Docker Container:
Step 1: Open Docker Desktop and click on containers
Step 2: Open Powershell and Run the following commands
Command 1: docker images
Command 2: docker pull hello-world
Command 3: docker images
Command 4: run hello-world
Command 5: docker images
Command 6: docker ps
Command 7: docker ps -a
Step 3: Open your docker and check if the hello-world is pulled there or not
![Docker step 3 output](image-5.png)

---

AIM: To build an image for sample web application using Dockerfile.

Step 1: Choose a Base Image
Step 2: Set the Working Directory
Use the WORKDIR command in your Dockerfile to set this working directory.

Step 3: Copy Application Files
Step 4: Install Dependencies
You can use package managers like apt-get, apk, npm, or pip depending on your application's needs.

Step 5: Expose Ports
Step 6: Define Startup Command
Use the CMD or ENTRYPOINT command to define the command that will be executed when the Docker container is run.

Step 7: Build the Image
Step 8: Run a Container
Step 9: Access the Web Application

E.g.
Go into your Directory using 'cd'
Copy File location
Open the directory in cmd OR
Command: code .
docker run -d p 80:80 my-html-website
docker build -t my-html-website
![Output](image-2.png)
Code:
![index.html](image-3.png)
![Dockerfile](image-4.png)
Run the code

---

AIM: To Understand Continuous monitoring and Installation and configuration of Nagios on Linux Machine.

Installation of nagios on linux machine:
https://support.nagios.com/kb/article/nagios-core-installing-nagios-core-from-source-96.html

---

AIM: To study Puppet Tools.

Theory and example

---

Drive Link for all the assignments:
https://drive.google.com/drive/folders/1w5ODT3JK5D42pDyX5048NwbvGr2nVpnb?usp=sharing
