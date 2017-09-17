# Creating a new repository on Github and local
### On Github
- Press `+` on the top right corner of the Github website to create a new repo with name `New-Repo`.
- Click *Clone or Download* button on the top right hand corner.
- Copy the url, like: https://github.com/kcchiu/New-Repo.git

### On local: Method 1
- Create a new folder with the same name `New-Repo`.  
- `cd` to the new folder `New-Repo`.  
- `git init`  
- `git local add origin https://github.com/kcchiu/New-Repo`  
- Create a new file on local  
- `git pull origin master`  
- `git push origin master`  
- Done.  

### On local: Method 2
- `cd` to the layer the repo is to be created.  
- `git clone https://github.com/kcchiu/New-Repo.git`
