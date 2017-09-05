Starting a new Wordpress from the [Wordpress Starter](https://github.com/Resilient-Labs/wordpress-starter)

Before you can duplicate a repository and push to your new copy, or mirror, of the repository, you must create the new repository on GitHub.
For example, for a resilient lab project, the lead developer would initiate a empty repo on github with the name matching the directory (folder) that the files will be saved in. Afterwards, you can follow the following commands:

1. Open Terminal
2. Create a bare clone of the repository by running the following in terminal:
```
git clone --bare https://github.com/Resilient-Labs/wordpress-starter.git
```
3. Mirror-push to the new repository by running the following in terminal:
```
cd wordpress-starter.git
```
```
git push --mirror https://github.com/exampleuser/new-repository.git
```
4. Remove the temporary local repository you created in step 1.
```
cd ...
```
```
rm -rf wordpress-starter.git
```

### Making the files your own
Open in text editor/IDE
Files to edit:
/site/web/app/themes/sage/assets/manifest.json
Change the line 25: "devUrl": "http://roots-example-project.dev"
to "devUrl": "http://new-project-name.dev"

/trellis/group_vars/development/vault.yml
Change line 7:
roots-example-project.com:
to
new-project-name.com:

/trellis/group_vars/development/wordpress_sites.yml
Change line 5:
roots-example-project.com:
to:
new-project-name.com
Change line 8:
- canonical: roots-example-project.dev
to:
- canonical: new-project-name.dev
Change line 10:
- www.roots-example-project.dev
to:
- www.new-project-name.dev
Change line 12:
admin_email: admin@roots-example-project.dev
to:
admin_email: admin@new-project-name.dev




