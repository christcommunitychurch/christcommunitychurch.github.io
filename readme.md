#Christ Community Church

Basic info: site built on [Jekyll](http://jekyllrb.com), a static site generator and developed and hosted on Github.

Mason is currently the admin of the repository, if you are interested in contributing to the website, please contact Mason at [masonfox22@gmail.com](mailto:masonfox22@gmail.com)

##Editing site prerequisites:
1. Speak with Mason Fox and or Chris
2. Have or set up a github account
3. Download the Github app
4. Download [Atom](https://atom.io) Text Editor (It is free and made by Github)
5. Understand usage of Github so we don't kill the site (will link video here)

####Windows User Notice

This process is setup for *mac users only at the moment*. Mason will write up the differences for Windows users. Windows users are mainly held up by the fact that Jekyll runs on the Ruby framework, which can be tricky to set up on a windows pc, although not impossible. This will be done in the future.

###Setting up Jekyll & Site directory:

1. Install Jekyll
  * Run: ~ $ gem install jekyll (may require sudo on Mac [ ~ $ sudo gem install jekyll ])
2. Tap the "Clone in Desktop Button" on the repository or clone from app
  * Save the file name as something small, like ccc
3. Navigate to the directory (Mine is in my home folder for easy access)
  * cd (change directory) into your git file (the one you just cloned)
  * Type ls to view all of the files

###Using Jekyll & Github:

There only two important Jekyll commands that we have at our disposal: Serve (s) and build (b).

These can be executed by:

> Jekyll (task)
* i.e s for serve or b build.

#####DO NOT EDIT THE SITE FILE
Editing the site file within the directory and then running jekyll serve will overwrite all of changes within this file. Jekyll compiles all of the files outside of the site file into the site file when jekyll s or jekyll b are executed. This site file is then served as the website. So, do not edit the site folder.

####Serve or s:
This will serve up a local environment for you to view the code. Jekyll's serve will automatically change text changes when a save is executed (this is not the case in styling or yml file changes)

*If changes to the config.yml file, rerun jekyll s to compile changes into site directory*

####Build or b
Build is used to compile the site directory. Editing the site file and generating the site file with build will overwrite all changes.

###Committing & Sending Pull Request
Users that have push access are the only users who are able to push changes to the website. As updating the repository is the only way to add and update content, users who do not have this push access will need to make a pull request to update these changes. Pull requests will send a notification to Mason showing that a change has been made. I will then check to make sure it is a valid change and push the request to the repository. To make a pull request, follow the instructions below:

1. Go to github app after your changes have been made
2. Commit changes (accurate commit info and summaries are expected)
3. Instead of "syncing", please submit a *pull request* to the master branch (should be default)

Github will block push access if you do not have push access and you attempt to push, so make sure you send a pull request. In time, push access or christcommunitychurch github account access will be granted to users who show sufficient understanding of the workflow of the website.

###How to edit/add weekly Sermons
The only necessary changes that need to be changed are located in the front matter within the index.html files and the sermons.html file. The front matter is located within the --- (content) --- of the page. This must be closed in order to work (you will see an error in the terminal and it will crash the localhost, don't worry, just close the front matter and it is fixed).

Elements in the front matter that need to be edited are:

>   - title: Example Title (The title of Sermon)<br>
    date: August 23, 2015 (The date of the Sermon, please keep Month Day, Year format)<br>
    summary: A sermon on the topic of Unity for our community (A very short summary of the message)<br>
    soundcloud: https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/220515139&amp;<br>
    klass: august (the month it is from, only put into the sermons.html page)<br>

###Explaining the Soundcloud API
Below is the process of adding a Soundcloud file to the website:

* Upload the sermon mp3 file to [Soundcloud](https://soundcloud.com).
* Add tags relating to the date (month, day, year)
* Add a summary for Soundcloud, the same as what will be on the website.
* Wait for upload... (Que elevator music)
* Click on the share button, select the embed button, and the second display option (has the sound graph)
* **Tricky Part Part 1:** Copy and paste the Soundcloud into the front matter
* **Tricky Part Part 2:** Trim the url from "https://" to the end of "&amp;" after the long list of numbers, but do not include the color segment of the embed. Use the front matter above as an example.
* Save these changes into the sermons.html as the earliest sermon and save it into index.html as the *only* Soundcloud embed.

Finaly, follow github procedures to commit and push/pull request changes to the repository.

###How to update the Blog
Blog posts are handled fluidly by jekyll. Any file that is in the "posts" directory will be compiled into the site directory. Below is the process of adding blog posts to the website:

* Add a new file within the "posts" directory with this name structure: year-month(number)-day-Example-title.md
    * Here is an example: /2015-07-23-Welcome-to-the-New-CCC-Website!.md
    * All words are broken up by a single "-"
    * Files must end in either **.md** or **.markdown**. This tells jekyll to compile the markdown in html
*  Add the correct front matter into the file. Below is an example:

> ---
  layout: post (it will **always** be a post)<br>
  title:  (The title of the post, typically the same as the file name)<br>
  date:   2015-08-23 10:30:00 (date and time)<br>
  images: images/home/launchsite.png (image files, should start with images/home/(your image file))<br>
  author: (Author of the Post)<br>
  excerpt: (The text that shows on the blog page that gives a short summary of the post)<br>
  ---

*Make sure to add the front matter marks --- (content) ---*

* Write text as you would in a text document like Microsoft Word
* After you are finished, after spell checking for errors and grammar, commit changes and send a pull request

###Other Info
*Please make detailed commits and summaries when working on large portions of code*

Test pushing
