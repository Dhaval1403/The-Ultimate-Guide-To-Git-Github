# The-Ultimate-Guide-To-Git-Github

_**What is Git & Github:**_

_Git can be very difficult to understand if you are using it for the first time. I myself had faced many problems when using it for the first time. But, with regularly using **Git and Github** now it seems a whole lot easier for me to work with. This is a simple guide for anyone who wants to learn git as efficiently and as fast as possible. I have tried my best to make this guide very easy to follow. So, without wasting any more time let's get started.. Shall we??_

_Git is simply a tool where developers collobarate and work together while Github is a place where all our code lives. We can create any number of repositories(projects) on github._

_Now, there are 2 ways to use git._

_1. Command Line (Highly Recommended)_

_2. Desktop Client (E.g, Github Desktop)_

_Before moving further let's get deep dive on what git actually is. Believe me guys, it's gonna be a lot of fun when you understand the actual purpose of using this tool._

_Let's assume that a web app is hosted somewhere in the world. The team that created this web app has 3 core members 'Alice', 'Bob' and 'Jack'. Each of them has the source code in their local machines (Laptops/Desktops). Now, let's say that 'Bob' has made some minor changes to one of the files and he thinks "Hmm.. It's not possible for me to go and inform my teammates everytime I made some change. So, is there anything that can do this workload for me". Well, yes there is. Hoorah!! You got it right.. It's **Git --> Version Control System**. In simple terms, git just keeps the track of our code. And Github is just a place where our code lives. So, now that we know what's git and github let's see how to use it._

_**Quick Note:**_

_1. Repository simply means project folder where our different files are present. It's just a naming convention that github uses._

_2. The project folder that lives on the github servers are called "remote repository". It's called remote because github hosts it somewhere in the world. We can access that repository by some unique url that github provides for us._

_3. The project folder that lives on our local machines are called "local repository". Pretty simple, right!! Ok, let's move on._

_**How To Use Git & Github:**_

_First of all, download git from the this link **https://git-scm.com** To verify that git is properly installed on your machine run **`git --version`** and it will give you the version number._

_Once the installation process has finished, open the **Git Bash** where we will write git commands. If you don't know where to find "Git Bash" here it is.._

_**Go to Desktop --> Right Click --> Select the option "Git Bash Here"**. And that's all, it will open a new terminal screen where we will write different git commands._

_Before we start make sure to complete all the below steps_

_1. Visit **https://github.com** and signup (if you haven't done already)_

_2. Make a new repository (e.g, Demo) by filling out the details._

_3. Create a new folder (e.g, Demo) on your laptop and create a new file "demo.txt" file inside that folder._

_4. Open **Git Bash** and cd into the folder that you created in the above step._

_Below are all the commands that we will learn:_

_**`git init`**_

_**`git remote add origin "your_github_repo_url`"**_

_**`git remote`**_

_**`git remote -v`**_

_**`git status`**_

_**`git diff`**_

_**`git add "filename"`**_

_**`git add .`**_

_**`git commit -m "Initial Commit"`**_

_**`git push`**_

_**`git config --global user.name "Your name"`**_

_**`git config --global user.email "Your email"`**_

_Don't worry. We will see what each command is in the following section. The fun part begins.. So, let's get started :)_

_**Example 1:**_

_Suppose, you have given same name to your local folder & your github repository i.e, **Demo**._

_Now, to use git commands we need to make sure that the folder we are using is a "Git Repository". For that purpose use the command **`git init`**. It will initialize your local folder into a git repository._

_**Disclaimer:** You need to initialize your local repository as a git repository otherwise the git commands will not work._

_You may have notice one thing over here i.e, we have an empty "demo.txt" file in our local folder. But, in the remote repository that you have created there is no such file. Hm.. Strange right?? Well the answer is simple. It's because git doesn't know where the remote repository is. For now git will just track the local files because it doesn't have any connection with remote repository. So, how to add the remote repository?? It's just a matter of 1 command._

_**`git remote add origin "your_github_repo_url"`** => It simply adds your remote repository and gives the name as **origin**_

_Now, to verify that your remote repository has been added properly or not just run the below command_

_**`git remote`** => It will give the name of the remote repository. For e.g, in our case it would be **origin**_

_**`git remote -v`** => It will give the name as well as the url of the remote repository. For e.g, in our case it would be **origin "your_github_repo_url"**_

_That's all.. We have successfully added our remote repository. Let's move on to the next step._

_Now, let's say you have modified the "demo.txt" file that you created earlier and added some text (For e.g, "Hello there!!!"). Git is smart enough to track the changes that you have made to the file. But, there's some gotcha over here. Let's find out_

_**`git status`** => It will show you the files in your Working Tree and the files in your Staging Area. In simple terms, it will show you exactly which files/folders have been modified. In our case it will show that **demo.txt** file has been modified._

_**`git add "filename"`** => It will add your file to the staging area. For e.g, **git add demo.txt**_

_**`git add .`** => If we add a '.' instead of filename then it will add all your files to the staging area. For e.g, **git add .**_

_Now, you may wonder that what's working tree & staging area?? So, let's find out._

_Basically, there are two important concepts over here.._

_**(Source of below definitions: https://medium.com/@lucasmaurer/git-gud-the-working-tree-staging-area-and-local-repo-a1f0f4822018)**_

_**Working tree**_

_The Working tree is the area where you are currently working. It is where your files live. This area is also known as the **`untracked area`** of git. If you make changes to files in your working tree git will recognize that they are modified, but until you tell git **`Hey pay attention to these files!!`** it won’t save anything that goes on in them._

_**Staging area**_

_The Staging Area is when git starts tracking and saving changes that occur in files. You tell git that I want to track these specific files, then git says okay and moves them from you Working Tree to the Staging Area and says **`Cool, I know about this file in its entirety.`**_

_Ok, now that you know about working tree & staging area let's move on to the next command._

_**`git diff`** => It will show the difference between a file in the staging area and file that's present in the working tree (Untracked file)._

_Let's understand **git diff** with a small example. Assume that your "demo.txt" file is empty. Now, run "git add demo.txt" command to add your file to the staging area. If our file gets added to the staging area then git will track all the changes that we have made. Add some text in your "demo.txt" file and before adding your file to the staging area just run the "git diff"._

_**`git commit -m "Your commit message"`** => It will save your changes to your local repository. It's generally good practice to include commit message so that you'll know what changes you have made. The **`-m`** flag is used to write down your commit message._

_Now, here's one more gotcha.. If you run the **`git commit`** command without saving your config variables, then git will throw out an error because they don't know that who's trying to make a commit. For that reason, we will need to add the config variables i.e, "name" & "email". So, how to add it?? It's very simple.. Just run the below 2 commands and that's it._

_**`git config --global user.name "Your name"`**_

_**`git config --global user.email "Your email"`**_

_How to verify that your config variables are added to the config file??_

_**`git config --list`** => It will list all the config variables. Search for your name & email and if you find out then it's been added to the config file._

_Now, up untill now all the changes that we have made lives in our local repository, right?? Remember we have also created a repository on github as well. In our local repository we do have a file named "demo.txt" but there's no such file in our remote repository. So, how to push the changes that we have made in our local repository to the remote repository. Let's find out.._

_(**NOTE:** When you'll run this command it will ask you for your github login credentials so just provide it)_

_**`git push origin master`** => It will just push all the changes from (**local -> remote**) repository. Remember, how we added our remote repository through "git remote add origin ..." command. So, the push command simply says that whatever we have in our local repository just push them in the remote repository. And in our case the remote is **origin**._

_You may also think think that what "master" is?? Don't worry, we will cover all those advanced topics in the Part - 2 of this series where we will cover topics such as.._

_**`git clone "your_github_repo_url"`**_

_**`git pull origin master`**_

_**`git branch`**_

_**`git branch -b "branch-name"`**_

_**`git branch -d "branch-name"`**_

_**`git checkout "branch-name"`**_

_**`What is fork??`**_

_**`What is a PR??`**_

_**`How to solve merge conflicts??`**_
