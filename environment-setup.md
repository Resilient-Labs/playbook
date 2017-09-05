# Environment Setup
Find here all the development dependencies and preferred development tools used in the Resilient Lab. If you run into any issues setting up or wish to make any changes to the setup process, please alert <a href="mailto:muigai@resilientcoders.org">Muigai</a> to the issue such that we can remedy the situation.

<ul>
    <li><a href="#vscode">VSCODE</a></li>      
    <li><a href="#atom">Atom</a></li>   
    <li><a href="#figma">Figma</a></li>  
    <li><a href="#filezilla">File Zilla</a></li>  
    <li><a href="#vbox">Virtual Box</a></li>  
    <li><a href="#vagrant">Vagrant</a></li> 
    <li><a href="#homebrew">Homebrew</a></li>
    <li><a href="#node">Node</a></li>  
    <li><a href="#yarn">Yarn</a></li>   
    <li><a href="#pip">Pip</a></li>   
    <li><a href="#ansible">Ansible</a></li>   
    <li><a href="#gulp">Gulp</a></li>   
    <li><a href="#bower">Bower</a></li>   
    <li><a href="#vagrantbindfs">Vagrant Bindfs</a></li>   
    <li><a href="#vagranthostmanager">Vagrant Hostmanager</a></li>   
    <li><a href="#createreactapp">Create React App</a></li>   
    <li><a href="#mongodb">Mongodb</a></li>
    <li><a href="#composer">Composer</a></li>   
    <li><a href="#mocha">Mocha</a></li>   
    <li><a href="#postman">Postman</a></li>
</ul>

## Bash Profile
Open Terminal and edit your local device's bash profile by running the following in terminal:
```
cd ~
```
to go to the home directory.
Next, we will create a file called `.bash_profile` (the dot means that it will be hidden).

Then use `nano` or `vi` in the Terminal. Unless you know what `vi` is, just use `nano`. To open up these files, you would use:
```
sudo nano .bash_profile
```
`sudo` makes sure that you will be able to save these files. Here, you can add aliases. `nano` or `vi` will automatically create a new file if it does not exist in your current directory in Terminal.
In nano, copy and paste this:
```
export PATH=/usr/local/bin:$PATH
```
After you are finished, press `Ctrl + O`, then `Enter`, and then `Ctrl + X` to save and quit. Finally, use
```
source ~/.bash_profile
```
to reload the Terminal and it will read what you put in those files.
```
open ~/.bash_profile
```
A small window should open up, in that text edit file see that you bash profile is updated.

## Applications

#### <span id="vscode">VSCODE</span>
Download [vscode] (https://code.visualstudio.com/)

#### <span id="atom">Atom</span>
Download [atom] (https://atom.io/)

#### <span id="#figma">Figma</span>
Download [Figma](https://www.figma.com/downloads)

#### <span id="#filezilla">File Zilla</span>
Download [FileZilla](https://filezilla-project.org/download.php?type=client)

#### <span id="#vbox">Virtual Box</span>
Download [VirtualBox](https://www.virtualbox.org/wiki/Downloads) >= 5.1.26

#### <span id="#vagrant">Vagrant</span>
Download [Vagrant](https://www.vagrantup.com/downloads.html) >= 1.9.8

## Global

#### <span id="#homebrew">Homebrew</span>
Homebrew installs the stuff you need that Apple didn’t
Install [Homebrew] (https://brew.sh/) by running the following in terminal:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

#### <span id="#node">Node</span>
Install [Node](https://nodejs.org) using Homebrew by running the following in terminal:
```
brew install node
```

#### <span id="#yarn">Yarn</span>
Install [Yarn](https://yarnpkg.com/ using Homebrew by running the following in terminal:
```
brew install yarn
```

#### <span id="#pip">Pip (the python package manager)</span>
Install [PIP](http://docs.ansible.com/ansible/latest/intro_installation.html#latest-releases-via-pip) by running the following in terminal:
```
sudo easy_install pip
```

#### <span id="#ansible">Ansible</span>
Install [Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html#latest-releases-via-pip) by running the following in terminal:
```
sudo pip install ansible
```

#### <span id="#gulp">Gulp</span>
Install the [Gulp CLI ("Command Line Interface")](https://gulpjs.com/) by running the following in terminal:
```
npm install --global gulp-cli
```

#### <span id="#bower">Bower</span>
Install [Bower](https://bower.io/) by running the following in terminal:
```
npm install -g bower
```

#### <span id="#vagrantbindfs">Vagrant Bindfs</span>
Install [Vagrant Bindfs](https://github.com/gael-ian/vagrant-bindfs#installation) by running the following in terminal:
```
vagrant plugin install vagrant-bindfs
```

#### <span id="#vagranthostmanager">Vagrant Hostmanager</span>
```vagrant-hostmanager``` is a Vagrant plugin that manages the ```hosts``` file on guest machines (and optionally the host). Its goal is to enable resolution of multi-machine environments deployed with a cloud provider where IP addresses are not known in advance

Install the [Vagrant Host Manager](https://github.com/devopsgroup-io/vagrant-hostmanager) by running the following terminal:
```
vagrant plugin install vagrant-hostmanager
```

#### <span id="#createreactapp">Create React App</span>
Install [Create React App](https://github.com/facebookincubator/create-react-app) Globally by running the following in terminal:
```
npm install -g create-react-app
```

#### <span id="#mongodb">MongoDB using Homebrew</span>
For rapid prototyping, as part of the MERN stack, for our database provider we use [MongoDB](https://www.mongodb.com/)

##### Steps to install in MongoDB:
1. Open the Terminal app and type: 
```
brew update
```

2. After updating Homebrew, install mongodb by running the following in terminal:
```
brew install mongodb
```

3. After downloading Mongo, create the “db” directory. This is where the Mongo data files will live. You can create the directory in the default location by running the following in terminal:
```
sudo mkdir -p /data/db
```
4. Make sure that the /data/db directory has the right permissions by running the following in terminal:
```
sudo chown -R `id -un` /data/db
```
Next you will be prompted to enter your password

5. Run the Mongo daemon (aka start the Mongo server), by running the following in terminal:
``` 
mongod
``` 
This should start the Mongo server.

6. Run the Mongo shell: 
Open a new terminal tab by pressing cmd+t and then with the Mongo daemon running in one terminal window tab, run the Mongo shell by running the following in terminal:
```
mongo
```
type mongo in another terminal window. This will run the Mongo shell which is an application to access data in MongoDB.

7. Exit the Mongo shell (terminal tab #2), reminder the last command you executed was mongo to run this terminal window, by running the following in terminal:
```
quit()
```

8. To stop the Mongo daemon (terminal tab #1) hit ctrl+c, reminder the last command you executed was mongod to run this terminal window

#### <span id="#composer">Composer</span>

1. Make sure that Homebrew is installed already
2. Install PHP by run each of the following in terminal:
```shell
brew update
brew tap homebrew/dupes
brew tap homebrew/php
brew install php71
brew install composer
```
3. To test installation, run:
```shell
composer -v
```
The terminal response should look like the following:
```shell
   ______
  / ____/___  ____ ___  ____  ____  ________  _____
 / /   / __ \/ __ `__ \/ __ \/ __ \/ ___/ _ \/ ___/
/ /___/ /_/ / / / / / / /_/ / /_/ (__  )  __/ /
\____/\____/_/ /_/ /_/ .___/\____/____/\___/_/
                    /_/
Composer version 1.5.1 2017-08-09 16:07:22
```
(or whatever the latest version is -
you will have to scroll upward to find it)

## Testing

#### <span id="#mocha">Mocha</span>
Install [Mocha](https://mochajs.org/) globally using npm by running the following in terminal:
```
npm install --global mocha
```

#### <span id="#postman">Postman</span>
Postman is used to share, test, document & monitor APIs  
Download [Postman](https://www.getpostman.com/)

