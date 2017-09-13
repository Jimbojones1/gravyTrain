## git

- git is a version control system so we can track changes to a project


#### Steps to set up a git repo

1. `git init` 
 - this initializes an empty git repository
2.  `git add <filename> or . (for all files)`
 - this command starts tracking files and stages them to be commited
3. `git commit -m "leave a message of what you just created"`
 - this command commits to the repo (builds a house with all your files at that current moment in time)

 * `git log` - will allow you to see your commit history

## github

- Github is on the internet, and it is exactly what the name says, it is a hub for git repositories
- Github allows developers to work on projects together and share code
- we 'push' our git repositories from our computer onto github to share with the world

### Connecting a git repo after we have git init in a folder in our computer
 1. go to github and select new repo 
 2. Now find the ssh address and copy it to your clipboard
 3. Go to the repo on your computer and run the command `git remote add origin 'address'` the word address is where you paste the ssh address from your clipboard.
 4. Type `git remote`, if you set everthing up correctly you should see `origin`
 5.  Now you are able to `git push origin master` in order to put your git repository onto github.


 ### Starting fresh from Github
 1. go to github and create a new repo
 2. Find the ssh address and copy it to your repo
 3. Go to your terminal in a folder that is not a git repository and run the command `git clone address`(once again the address is where you paste the ssh address)
 4. So now you have cloned that repo down to your computer, and you just have to `cd` into the folder
 5. no need to `git init`, the clone took care of that for you, so now you can just add and commit like normal.  And when your ready to push up run `git push origin master`


 ** To pull down from github, run the command `git pull origin master`
 - This takes whatever is on github and puts it on your computer



