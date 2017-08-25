# Environment Setup:
Find here all the development dependencies and preferred development tools used in the Resilient Lab. If you run into any issues setting up or wish to make any changes to the setup process, please alert <a href="mailto:muigai@resilientcoders.org">Muigai</a> to the issue such that we can remedy the situation.

## Bash Profile
Open Terminal and edit your local device's bash profile by running the following in terminal:
```
open ~/.bash_profile
```
A small window should open up, in that text edit file, copy and paste this:
```
export PATH=/usr/local/bin:$PATH
```

## Applications

#### VSCODE
Download [vscode] (https://code.visualstudio.com/)

#### Atom
Download [atom] (https://atom.io/)

#### Figma
Download [Figma](https://www.figma.com/downloads)

#### File Zilla
Download [FileZilla](https://filezilla-project.org/download.php?type=client)

## Global

#### Homebrew
Homebrew installs the stuff you need that Apple didn’t
Install [Homebrew] (https://brew.sh/) by running the following in terminal:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

#### Node
Install [Node](https://nodejs.org) using homebrew by running the following in terminal:
```
brew install node
```

#### Create React App
Install [Create React App](https://github.com/facebookincubator/create-react-app) Globally by running the following in terminal:
```
npm install -g create-react-app
```

#### MongoDB
For rapid prototyping, as part of the MERN stack, for our database provider we use [MongoDB](https://www.mongodb.com/)

##### Steps to install:
1. Open the Terminal app and type: 
```
brew update
```

2. After updating Homebrew, install mongodb by running the following in terminal:
```
brew install mongodb
```

3. After downloading Mongo, create the “db” directory. This is where the Mongo data files will live. You can create the directory in the default location by running 
```
mkdir -p /data/db
```
Make sure that the /data/db directory has the right permissions by running
```
sudo chown -R `id -un` /data/db
```
Next you will be prompted to enter your password

5. Run the Mongo daemon (aka start the Mongo server), by running the following in terminal:
``` 
run mongod
``` 
This should start the Mongo server.

6. Run the Mongo shell: 
Open a new terminal tab by pressing cmd+t and then with the Mongo daemon running in one terminal window tab, run the Mongo shell by running the following in terminal:
```
mongo
```
type mongo in another terminal window. This will run the Mongo shell which is an application to access data in MongoDB.

7. Exit the Mongo shell by running the following in terminal:
```
quit()
```

8. To stop the Mongo daemon hit ctrl+c

## Testing

#### Mocha
Install [Mocha](https://mochajs.org/) globally using npm by running the following in terminal:
```
npm install --global mocha
```

#### Postman
Postman is used to share, test, document & monitor APIs
Download [Postman](https://www.getpostman.com/)

