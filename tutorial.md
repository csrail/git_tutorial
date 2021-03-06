#Project Notebook

I hope you have been taking electronic notes, because in this project we are going to upload these notes onto github using git.

* Lets clarify any confusions:
	* "git" refers to a program that carries out version control
	* "`.git`" refers to a special folder
	* "github" refers to a website

**Warning:** Put your [Imagination Cap](https://www.youtube.com/watch?v=NaSd2d5rwPE) on - we will be using a lot of analogies and metaphors.

**Warning** Text on a page can only teach you in a linear fashion, but git cannot be understood linearly. In short, I encourage you to stick around and read this material once through from top to bottom, then again in any order bouncing around the page till it makes sense.

##Version Control Systems
When you are writing essays or hacking away at code, if you get things right the first time - without making errors or the need to make drafts - then you are probably a prodigy. For mere mortals though, you will constantly need to do revisions of your work. 

When you hit *save* in a text-editor, the only thing the text-editor remembers is the final result. **Save does not remember all the changes in between**. 

This is where version control systems come in (hereby known as **VCS**).

Version control systems are:
* smart enough to remember what differences were made from the most recent entry to the latest entry. 
* not smart enough to know what *you* consider is the most recent entry. You have to label which files the VCS should treat as "most recent".

**Git** is a popular and powerful VCS that many web developers use. Its mascot is this unfortunate [ugly / cute thing](https://assets-cdn.github.com/images/modules/logos_page/Octocat.png).

In summary, to establish Git as our VCS we have to understand that:
* first: we create a `.git` in our folder to record changes
* second: we need to tell `.git` what to record and then to archive that record
* third: we are setting up a folder (called a repository) on github to keep all our records online

##Terminology: where and what are these things?
###.git
* Your `.git` folder is like the **Bag of Holding** and a **Mimic Chest** combined:
	* `.git` is like a *bag of holding* because it is able to store a lot of information but is only present as this tiny, hidden and inconspicuous folder in your root directory
	* `.git` is like a *mimic chest* because it captures and stores all the changes you do within the root directory

![Bag of Holding](http://url/to/img.png)
![Mimic Chest](http://url/to/img.png)

* FAQs:
	* What does *root directory* refer to?
		* directory refers to folder and root refers to "beginning"; therefore the root directory is where all your files are being kept. Think of your root directory as the biggest [russian doll](https://youtu.be/-xMYvVr9fd4?t=18s) and all other files inside it are the smaller dolls. If you are inside your root directory, you can see all the files involved in it; if you are outside your root directory, all you see is the root directory's name.
		* `.git` must exist within the root directory otherwise you will run into many errors and problems associated with pathing.
		* there also, should only ever be one `.git` folder per project otherwise you will again, run into many errors and problems associated with pathing.
	* What does *hidden* mean?
		* if you type `ls` you will see the usual list of files and folders
		* then if you type `ls -a` you should see files and folders pop up with a `.` in front of them - these are your hidden (inconspicuous, occult, scheming) files. These hidden items are usually not to be tampered with.
	* What counts as a *change*?
		* changes include adding / deleting folders, files and even stuff written INSIDE your files - all of this your `.git` folder, using the programs inside it, picks up.

###Depots: Local vs Remote
* A depot is a "place for the storage of large quantities of equipment, food, goods" - or in our case, data. 
* There are local and remote depots:
	* your personal computer or laptop is a local depot
	* a server or website is a remote depot

* FAQs
	* What makes the depot local?
		* the depot is local because it is both *tangible* and *offline*:
			* **tangible** means we can access the contents of the depot by just turning the device on eg, a personal computer, laptop, mobile phone
			* **offline** means we can access the contents of the depot without an internet connection
	* What makes the depot remote?
		* the depot is remote because it is *in a land far far away*
			* **in a land far far away** means your device cannot access the contents of a depot unless you have an internet connection
	* How do I pronounce [depot](https://www.youtube.com/watch?v=_UYiCjmrGC4)? The "t" is silent.

###How git commands work:
* A typical git command is: `git add .` and this is the breakdown:
	* pretend our `.git` folder is like a dog. And we have named our dog "Steven"
	* when you type `git add .` it's like saying `Steven fetch ball`
		* When you say the name `Steven` you are talking to your dog. When you say `git` you're talking to your `.git` folder
		* When you say `fetch`, you are using a verb to tell your dog to take action. When you say `add` youre are telling your .git folder to take action
		* When you say `ball` you are telling your dog to fetch the ball. When you say `.` you are telling your .git folder to add all the files and folders within the current directory
	* git syntax in short:
		* `name` | `verb` | `noun`
		* `program` | `action` | `object` or `destination`

* Commands we will be running in order:
	* `git init`
		* read as: `git` | `init` |
	* `git add .`
		* read as: |`git`|`add`|`.`
	* `git commit -m "message"`
		* read as: |`git`|`commit`| `-m "message"`
	* `git remote add origin https://github.com/your_username/notes.git`
		* read as: | `git` | `remote add` | `origin https://github.com/your_username/notes.git`
	* `git push origin master`
		* read as: |`git` | `push` | `origin master`


If you dont set a remote location to point to:
`git remote` doesn't show anything

once you do set it,
`git remote` shows `origin`
`git remote show origin` show a url that you have set


##My version control system works locally, why do I have to put anything online?
Good question
* The main reason is collboration
	* you can work on the project remotely while another programmer on the other side of the world can work on the same project remotely too

* Other reasons:
	* visually see changes done from one historical entry to another
	* having a backup
	* sharing your work for others to see, debug or praise!

##What is a README.md file and do I have to make one?
* It's like a contents page.


### Produce instructions for project:

- [ ] **Remote instructions - things done in your web browser only:**
- Open your web-browser
- Go to [github website](https://github.com/) and log in to your account.
- Click on *New Repository*
- In the text field beneath *Repository name*, type in the name `my_notes` (or whatever you want your folder containing your notes to be called)
- Add an *optional description* to the repository you are about to create
- Ensure that the the box *Initialize this repository with a README* is **unticked**
- Click the *Create New Repository* button
- [ ] **Local instructions - things done in your command line only:**
- Note for users that directory == folder
- Open your command line interface
- Enter your `the_odin_project` directory
- Create a new directory named `my_notes` (this should be exactly the same name as the repository)
- Move any electronic notes you have made into your `my_notes` directory
- Enter your `my_notes` directory
- Type `git init`
- Type `git add .`
- Type `git commit -m "message"`
- Type `git remote add origin https://github.com/your_github_username/my_notes_directory_name.git`
- Type `git push origin master`
- Enter your github username
- Enter your password (this is invisible but registers your input)
- Go to https://github.com/your_username/my_notes and if it left open, refresh it.
- You should now see your very own notes uploaded onto your github account.

Add encouragement and to cycle through the `git add .`, `git commit -m "message"` and `git push origin master` commands at the end of each study or note taking session.
Tell them that the "git environment" has been established and to forget about `git init` and `git remote add (url)` until they need to make another project.

### Additional
- [ ] Produce images:
- **Github screenshots for following**
- Bag of Holding
- Mimic Chest
- [ ] **Archive guide - to be adjunct material to project**
