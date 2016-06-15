#Project Notebook

I hope you have been taking notes, because in this project we are going to use git to upload our notes onto github.

**Warning:** Put your [Imagination Cap](https://www.youtube.com/watch?v=NaSd2d5rwPE) on - we will be using a lot of analogies and metaphors.

##Version Control Systems
When you are writing essays or hacking away at code, if you get things right the first time - without making errors or the need to make drafts - then you are probably a prodigy. For mere mortals though, you will constantly need to do revisions of your work. 

When you hit *save* in a text-editor, the only thing the text-editor remembers is the final result. ***Save* does not remember all the changes in between**. 

This is where version control systems come in (hereby known as VCS).

Version control systems are:
	* smart enough to remember what differences were made from the most recent entry to the latest entry. 
	* not smart enough to know what *you* consider is the most recent entry. You have to label which files the VCS should treat as "most recent".

**Git** is a popular and powerful VCS; its mascot is this [ugly / cute thing](https://assets-cdn.github.com/images/modules/logos_page/Octocat.png). There are other VCSs available but they are pretty old school: ~~Mercurial, Bazaar or Darcs~~. 

* Lets clarify any confusions:
	* "git" refers to the version control system we will be using
	* `.git` refers to a folder
	* github refers to a website

To establish Git as our VCS we have to understand three things:
* that we 
*






##Terminology: where and what are these things?
###.git
* Your `.git` folder is like the **Bag of Holding** and a **Mimic Chest** combined:
	* `.git` is like a *bag of holding* because it is this tiny, hidden and inconspicuous folder in your root directory
	* `.git` is like a *mimic chest* because it captures and stores all the changes you do within the root directory

* FAQs:
	* What does *root directory* refer to?
		* // where you want your project to start
		* // `.git` must exist within the root folder otherwise you run into errors and problems
	* What does *hidden* mean?
		* //reference to ls
		*// then type ls -a
	* What counts as a *change*?
		* // includes adding or deleting folders, files and even stuff written INSIDE your files

###Depots (Local vs Remote)
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
	* How do I pronounce [depot]()?






###How git commands work:
* A typical git command is: `git add .`
* And this is the breakdown:
	* pretend our `.git` folder is like a dog. And we have named our dog "Steven"


* `git add`
* `git commit`