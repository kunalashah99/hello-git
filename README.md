# Intro to Git

## The Basics
<p align="center">
  <img src="git-workflow.jpg" alt="diagram showing git workflow"/>
</p>


### Installing git
If using Linux or MacOs, `git` should probably be present already. If not, follow the insttructions [here][6].

For Windows, download the installer from [here][5].

### Cloning a repo
Click on the green `Code` button on the repo page, copy the `https` link. Open a terminal and move to desired folder. Then run the `git clone` command along with the copied url to create a local copy of the repo.

So, to clone this repo, the command would be
```bash
git clone https://github.com/hsrwrobotics/hello-git.git
```
### Pushing to a repo
The three step process
1. `git add <files paths>`
2. `git commit -m "<commit message>"`
3. `git push <remote> <branch>`


For this repo, add your name to the [Participants](#participants) section of this markdown file and save it. Then
```bash
git add README.md
git commit -m "First commit"
git push origin main
```



### Pulling a repo
Make sure you have the latest files locally, before pushing
```bash
git pull origin main
```

## Hosting a static website

I set up a simple portfolio template for you to use.

### Forking a repo
![fork icon](https://github.com/channelCS/github-buttons/blob/master/2x/github_fork.png)


Click on the `Fork` button  to create a remote copy first. Then go to this forked repo page and clone it(Notice the url of the fork is different from the original). 

### Creating a branch
We will create a branch called `pages` which will used to host the website(basically what is contained in the `website` folder in the repo)
The easiest way
```bash
git checkout -b pages
```

### Pushing to branch
In order to use the `Github pages` feature, the `index.html` needs to be located either in the root directory or in a `docs` folder. So, let's make this change first. Make sure you are in the `pages` branch of your forked repo.(You can check this by running `git branch` command from the terminal, the current branch that you are on should be highlighted). Rename the folder using git and then push the chnages to the correct branch
```bash
git mv website docs
git commit -m "updating webpage"
git push origin pages
```
Head over to Github page on your browser, and go to `Settings` -> `Pages` tab. Set `Branch` to pages and click on `Save`. And now we wait... In about 3-5 minutes, you should see a message that says your website is live(Refresh your page if you dont see a message even after 5 minutes). Click on the url to open it up. 

The urls normally follow the format `hhtps://<github userID>/<Repo name>/`


Open the `html` file and edit it to your needs(like replacing `NAME HERE` with your own name). Push these changes and watch the page rebuild to display the updated info.
```bash
git add .
git commit -m "updating webpage"
git push origin pages
```
> `.` is used to when you want to select everything. So, if you have a lot of files that need to be push, you could use `git add .` or even `git commit -a`  to make things easy, although this is not recommended until you actually have a proper `.gitignore` set up.

## Participants
- Thomas

## References
- [Particles JS library][3]
- [Particles JS configurator][2]
- [Some Github portfolio inspirations][8]
  - [Ben's portfolio][4]
- [Bootstrap footers][1]
- [Icon8][7]




<!-- Reference urls -->
[1]: https://getbootstrap.com/docs/5.1/examples/footers/
[2]: https://vincentgarreau.com/particles.js/
[3]: https://github.com/VincentGarreau/particles.js
[4]: https://benrogers.dev/
[5]: https://git-scm.com/download/win
[6]: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
[7]: https://icons8.com/
[8]: https://github.com/emmabostian/developer-portfolios