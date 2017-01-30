Github-Workflow
===============

Process for contributing to projects.

##Client Communication and Deal Stage
1. Every communication with a client must be logged in Hubspot. You should be using the Hubspot crm plugin for gmail or outlook. This will keep all of our communication and files in one location.
2. As a client progresses, please move them to the appropriate stage of the lab pipeline.
3. Once a deal reaches the development phase of the pipeline Muigai or Leon will create a new repository and Github project for that client.

##Github Project
1. Every project in the development stage on Hubspot must have a corresponding Project/Repo on Github - owned by Muigai or Leon.
2. Use the Github Project Kanban board to plan tasks for that project.
3. Enter every task to be completed into the Icebox column.
4. Sprint plan once a week to chose which items make it into the sprint column. Move them to the sprint column.
5. Turn every item in the sprint column into an issue.
6. Assign the issue to yourself and move it into the working column.

##Getting Work Done
1. Fork the repo (on github) and clone it to your Desktop ```git clone <repo url>```
2. Add the upstream (keeps track of changes on main repo) ```git remote add --track master upstream git://github.com/upstreamname/projectname.git```
3. Get the code from upstream ```git fetch upstream```
4. Merge the code from upstream into your master ```git merge upstream/master```
5. Create a new branch to get work done (use the issue number to name the branch ex. iss15 would be if you were working on the 15th issue) ```git branch iss15```
6. Checkout branch you created, so you can start working on it ```git checkout iss1```
7. MAKE YOUR CHANGES (keep them small and don't make goofy commits) - if you use a lot of commits you will need to squash them to keep your commits clean
8. Commit your changes ```git commit -a -m 'added whatever [issue 15]'```
9. Push your commits ```git push origin iss15```
10. Pray - msg Muigai or Leon if it did not work
11. Move back to master ```git checkout master```
12. Pull any changes ```git pull```
13. Repeat

##Submitting Pull Request
1. Go to your forked repo on github
2. Locate the branch you created
3. There should be a green button asking you to submit a pull request - click it
4. Enter as much detail as possible to describe what changes you made and submit
5. Relax
6. Muigai or Leon will approve your pull request in time
7. Assign yourself another issue and move it into the working column - repeat above!





jekyll-vagrant
==============

Environment for developing jekyll projects locally.

## Setup
1. Make sure Vagrant and virtual box-sizing are installed.
2. Clone this repository
3. Open command prompt to location of the Vagrantfile and run ```vagrant up```
4. Jekyll and all it's dependencies are installed!

## Existing Jekyll Projects
1. Copy the projects folder to the folder that contains the vagrantfile.  
2. Open a command prompt to location of the Vagrantfile and run ```vagrant ssh```
3. Once on the VM prompt ```cd /vagrant/<YourProjectFolder>```
4. Start the jekyll server ```jekyll serve --host 0.0.0.0```


## New Jekyll Projects
1.  Open a command prompt to location of the Vagrantfile and run ```vagrant ssh```
2.  Once on the VM prompt ```cd /vagrant```
3.  Create new site with ```jekyll new <sitename>```
4.  cd into new folder ```cd <sitename>```
5.  Start the jekyll server ```jekyll serve --host 0.0.0.0```
6.  Visit Site in Browser ```localhost:4000```
