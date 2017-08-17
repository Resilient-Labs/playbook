###### [main](README.md)
Wordpress on Digital Ocean Staging
===============

So you want to run a wordpress instance on Digital Ocean? Maybe for staging to show off to the client? Well you’re in luck, setting that up is as easy as pie. Follow these instructions to get there! Vamos!

## Prerequisites
- A <a href="https://www.lastpass.com/" target="_blank">Lastpass Account</a>
- The Lastpass Chrome Extension installed on your Google Chrome browser
- Terminal installed on your device

## Logging into Digital Ocean

1. To start, ask the Lead Developer to share the Lastpass login credentials for the Dev 
Team’s Digital Ocean Account. Make sure those credentials are shared with you before 
to the next step.
2. Now with the Lastpass login credentials in hand, log in at digitalocean.com using 
the Lastpass extension, be sure to use this as the username: 
dev+digitalocean@resilientcoders.org
3. If login was successful, you should be brought to a screen that shows you a list of Droplets. Don’t worry about the term droplet but if you’re curious to know, here’s the skinny: Digital Ocean calls its virtual private servers Droplets; each Droplet that you spin up is a new VPS for your personal use.

## Creating a Droplet
1. Find the Create button. Click that dropdown and then click Droplets to start the process of creating a new droplet. 
2. On the “Create Droplets” screen, you will have a few options to choose from, here’s 
what we normally go with:
    - #### Choose an Image
        Click the tab for 'One-click apps' and then select Wordpress 4.8 on 16.04 
        option (this is the latest version at the time of writing this)
    - #### Choose a size
        Select the option that is priced at $10 / mo $ 0.015/hour and comes with 1GB / 1 CPU , 30GB SSD Disk, 2 TB Transfer. This will be more than enough for our needs
    - #### Skip Add block storage
    - #### Choose a datacenter
        Let’s keep this one on American soil. Select New York. Either 1, 2 or 3 works, your choice !
    - #### Select Additional Options
        Select Monitoring alone. Gotta keep an eye on the activity on this server
    - #### Skip Add your SSH keys
    - #### Final Steps 
        Make sure How Many Droplets is at 1 and then Choose a hostname. Good examples of site names are lower case and multiple words are separated by hyphens while also including the company or project name. 
    
        An example droplet name: resilient-coders
    - #### Click Create
    
## WordPress Installation
1. At this point, you should be brought back to that droplet list screen with your 
droplet firing up. Once that is all set, copy and paste the IP Address for your droplet into the browser to visit the Wordpress instance. If all worked well, the IP Address should show a picture of a shark swimming in the Digital Ocean with the message: “Please log into your droplet via SSH to enable your WordPress installation.“ Ping the Lead Developer to fetch the ssh credentials that were sent to the dev team’s gmail account.
2. Now the fun begins, with the ssh credentials, open your terminal 
    #### SSH into the Virtual Private Server (Droplet)
    ```
    ssh <username>@<ip-address>
    ```
    an example of what this might look like, where the username is root and the ip address is 104.236.201.235: 
    ```
    ssh root@104.236.201.235
    ```
    #### Enter Current UNIX Password
    Copy and paste the password sent by the Lead Developer after being prompted for 
    the password. (Remember terminal hides passwords, so don’t worry if you cannot see 
    it after pasting it.)
    #### Enter Current UNIX Password Again
    Next you will be prompted for the (current) UNIX password, paste that same password that you pasted previously into the terminal and press enter.
    #### Enter new UNIX Password
    Now you should be prompted to enter a new UNIX password then following that retype 
    the new UNIX password. Be sure to put in a secure password that you can remember and 
    record it down in Lastpass. We recommend generating a random password. 
    #### WordPress Installed
    If all goes well, the terminal should read: Wordpress has been enabled !
    
    Return to the browser at the IP Address for your droplet and go through the 
    Wordpress Install. Happy WordPressing !
