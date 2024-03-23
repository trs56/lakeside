---
title: Get Started Today!
toc: toc-getstarted.html
print: print-button.html
---

Step by step process for beginners, new to GitHub. It's easy to create an account and get started today.

### Use a Team/Pro Account
Even as a total newbie to GitHub, I recommend this low-cost option so you can use a custom domain name and publish from a private repo in a separate Team account instead of publishing from a public repo on your personal account.

### Editing and Publishing
It is important that you understand the process. This repository has two branches. All editing is performed on files in the top level **edit** branch. When you're done and ready to publish, you will then **pull** your updates into the **publish** branch for the automatic **Pages Build and Deploy** action. This may not be SOP for GitHub pages but it works for me.

### Make it Your Own
All you need to do is edit a few files for starters. And if you're like me and never really done this kind of thing before, open those files in the editor to see just how easy it is to use GitHub "markdown" formatting for your content.

For me, the best way to learn has been by example, so you may want to keep this page and the design page as references. You can do that without including them in your site. You will notice that much of the fancy stuff I do is with HTML.

See [Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax){:target="_blank"} for more on markdown syntax. All of GitHub is well documented in their help pages.

### Step 1: Create the Repository
1. Click here to open [TR-Systems/lakeside](https://github.com/tr-systems/lakeside){:target="_blank"} on GitHub in a new browser tab. 
2. Click the button in the upper right to <span style="border:2px solid silver;border-radius:6px;padding:0 4px;background-color:lightgreen;">Use this template</span> and select create new repository.
3. **Create a New Repository** appears. **Owner** will default to your GitHub userid. Switch to your Team account if using one. Give your repo a **short web-friendly name** like "web" or "mycoolthing" since the repo name is the top level path in the url to your site. **DO NOT include all branches.** If using a personal account, you must create a public repo, and only one of your public repos can have a website. This restriction does not apply for Team accounts.
4. Click <span style="border:2px solid silver;border-radius:6px;padding:0 4px;background-color:lightgreen;">Create repository</span>
5. The repo will be copied and created. You are looking at it now.
6. Create the **publish** branch by clicking on the **edit** branch button, then **type "publish"** and then **click the line** that says **create branch publish from edit**, as shown here by clicking this button:

<div class="dropdown">
<button type="image" onclick="myButtonClick()" style="margin-left:24px; margin-bottom:6px; padding:0;">
<img src="images/edit.png">
</button>
<div id="myButtonContent" class="drop-content" style="position:relative; margin-left:24px; background-color:aliceblue; box-shadow:none; padding:0;">
<img src="images/createbranch.png">
</div>
</div>

The publish branch is now ready to receive updates from the edit branch. You are looking at it now.

Click that button again and SWITCH BACK TO THE EDIT BRANCH.

### Step 2: Edit config.yml
Fill in your header and footer information and define the links you want to provide for the three buttons in the upper right corner of the page. Follow the instructions and tips provided in the file.

<span style="border:2px solid silver;border-radius:6px;padding:0 4px;background-color:lightgreen;">Commit</span> your changes.

Now is a good time to skip down to Step 7 to initiate a **pull request** into the **publish** branch and then **Step 8** to configure your repository and build your new website so you can see the changes you just made and confirm the process works for you.

Then come back to finish the job of making it your own.

### Step 3: Edit index.md
This is your home page. Remove the **front matter** if you do not want a toc or print button. **Note:** If you do not specify a page **title** in the **front matter** of any page, always start your content with a markdown heading for Jekyll to use as the page title shown in the browser tab, and of course, at the top of the page.

### Step 4: Edit about.md
Tell the world what this is all about.

### Step 5: Edit _includes/site-menu.html
Give users an easy way to navigate your site. Remove the links for the design and get started pages if you have excluded them from your site in the config file.

### Step 6: Edit _includes/toc-homepage.html
Either update or delete this file if you will not using it.

### Step 7: Pull Changes into Publish
This process will create a **pull request** to apply your changes to the files in the publish branch. There are other ways to initiate the pull request but they all end up at the same place.

1. Switch to the **publish** branch. You will see that it is <span style="color:#069;text-decoration:underline;">N commits behind</span> the edit branch depending on how many "commits" you performed in the steps above. **Click on that link**.
2. **Comparing Changes** appears. Scroll down to view the changes.<br>
Click <span style="border:2px solid silver;border-radius:6px;padding:0 4px;background-color:lightgreen;">Create pull request</span>
3. **Open a Pull Request** appears, where you can enter a title (required), optional description and view the changes again.<br>
Click <span style="border:2px solid silver;border-radius:6px;padding:0 4px;background-color:lightgreen;">Create pull request</span> again
4. GitHub checks to see if there are any conflicts between the two branches. There won't be as long as you never edit and commit any changes directly to the publish branch.<br>
Click <span style="border:2px solid silver;border-radius:6px;padding:0 4px;background-color:lightgreen;">Merge pull request</span>
5. Click <span style="border:2px solid silver;border-radius:6px;padding:0 4px;background-color:lightgreen;">Confirm Merge</span>
6. After you have executed the next step, each time you merge changes into the publish branch, GitHub will run the **Pages Build and Deploy** action automatically.

### Step 8: Configure GitHub Pages
You only need to do this once.

2. Click the repo  <i class="material-icons" style="font-size:14px;">settings</i>**Settings** button.
3. In the nav bar on the left, click **Pages**
4. **GitHub Pages Build and Deployment** appears.<br>
Select **Deploy from branch**, **publish** /root<br>
Click **Save**.
5. GitHub will kick off the Pages Build and Deploy action
6. Click on **Actions** to watch that process run
7. Go back to **Settings/Pages** and click the link to visit your site

Voila! Websites made easy! Ha! Your job has just begun.

But that's it, in a nutshell, apply changes to the edit branch and pull them into publish.

---

### Technical Reference
#### <span style="color:#069">_layouts/default.html</span>
Defines the HTML structure of your pages and is where the values of the config variables are placed on the page.

#### <span style="color:#069">assets/css/style.scss</span>
Defines how all content appears on your pages and is referenced in the <head> section of **default.html**.

#### <span style="color:#069">images</span>
Cut and crop your image files way down in size and resolution before uploading to this folder and using them in your pages. You can fine-tune the size of an image on a page using width, height or percent settings when you reference it. There is much more to this topic than I can possibly share with you here. Just don't upload full resolution pics from your camera.

#### <span style="color:#069">_includes</span>
This is where you will define your **site menu** for all pages and a **table of contents** for any page that warrants, which are referenced in **default.html**. The **site menu** is called out in the **config** file using the **menu** variable. A **toc** is called out in the front matter of the page using the **toc** variable.

#### <span style="color:#069">print-button.html</span>
If you want the print button to appear in the header, call it out in the front matter of your page using the **print** variable.

#### <span style="color:#069">button-script.html</span>
This is the script that displays the dropdown list for the site menu and toc buttons when clicked and is placed in the <head> section of **default.html**. Currently, it will only hide the toc content when you click elsewhere on the page. So for now, the only way to hide the site menu is to click on it again. This is a work in progress and a major change in the script and methods being used is required. Still learning.

---

#### Google Analytics
Setting up Google Analytics is easy. All you need to do is create an account and then define a "stream" for it to monitor, that being the url for your website. That will provide you with the "code snippet" that you need to put into an html file in the **_includes** folder and then call it out using the **google-analytics** variable in the config file.

So until then, please be sure to comment-out that variable in your config file. Thank you!

---

## Develop on Windows
*Last updated: 2024-02-22*

1. Install [Git Bash](https://gitforwindows.org/){:target="_blank"} and [GitHub Desktop for Windows](https://desktop.github.com/){:target="_blank"} (all good)<br>
Git has many install options. Take the defaults but do not include *Scalar support for Large Repositories*.
2. Install [Ruby](https://rubyinstaller.org/){:target="_blank"} (all good).<br>
Take the defaults and be sure to run the ridk process at the end. I installed Ruby at c:\Ruby32. This app is huge.
3. Open Command Prompt or Git Bash and confirm:
```
ruby -v returns Ruby 3.2.3 (2024-01-18 revision 52bb2ac0a6) x64-mingw-ucrt<br>
gem -v returns 3.4.19
bundle -v returns Bundler version 2.5.6
jekyll -v returns jekyll 4.3.3
```
4. Clone the edit branch of your repo using GitHub Desktop
5. Add **Gemfile** to the root folder
```
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
gem "webrick"
gem "wdm"
```
6. Open Git Bash and cd to your repo root folder (edit branch)
7. Run **bundle install**<br>
Ok, 98 gems installed, a brick of web I guess.
8. Run **bundle exec jekyll serve**

The site now builds and is served locally from the **_site** folder, where you will see your markdown files converted to html. [Check it out!](http://localhost:4000)

1. You can now add or update files in the local clone of the repository ***on the fly*** with the jekyll server running and see them instantly in your browser with a page refresh.
2. When you're done, review your changes using GitHub Desktop and then **push** them up to the **edit branch** on GitHub.
3. Then, on GitHub, create the pull request into the publish branch for "pages build and deploy".

### Editing on Windows
I'm using [Notepad++](https://notepad-plus-plus.org/downloads/){:target="_blank"}. I like the folder workspace on the left, and how it highlights content when editing. It also has tabs for editing multiple files. My only tip is to set a block cursor and have tabs converted to spaces. You will have to dig through the settings to find those.

---

## Develop on Ras Pi
2-20-24: Ok, here we go, starting with a fresh Ras pi 4 B.

1. Install Ruby and Jekyll per the doc referenced above and confirm:<br>
ruby -v returns 3.1.2p20<br>
jekyll -v returns 4.3.3
2. Cd to local **github** folder and run **git clone 'url to your website repo'**
3. Add **Gemfile** to the root folder, without "wdm"
```
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
gem "webrick"
```
4. Cd to the root folder of your repository and run **git fetch** to get some changes between step 2 and now
5. **sudo su**
6. Run **bundle add webrick**<br>
Adds a LOT of Jekyll gems, themes and other web stuff, a brick of web I guess.
7. **exit** out of su
8. Run **bundle install**<br>
Ok, 97 gems now installed (one less than Windows, no wdm)
9. Run **bundle exec jekyll serve**
10. Yay! It works! 

FINALLY, for the first time in this never ending all time consuming silly winter project of mine, something actually worked on the first attempt! Without a single rat hole to chase down first.

---

Fun stuff... hope it is for you, too!

---

End of Document
