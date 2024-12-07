# Portfolio_Template

testing with r studio build option not displaying. 


This is for the 12th commit to the master branch. 
This has steps from creating repo, creating project, uploading files for site build, render website locally, pushed to github and set settings to render site
then has steps to add a new tab. 


For the following commits I will try and work with python code, which is proving to be challenging but it is something that needs to happen because it is what has been causing the most trouble with gh-pages, and also when I added python code it threw some errors



This is current notes for this ( not included in the 12th commit to the master branch)

Portfolio template steps
1.	Video to create the github repository with readme.md file, and how to create r studio project
a.	The r studio project created the .gitignore and Portfolio_Template.Rproj files
i.	This seem to have settings required for r studio to connect to github.
2.	Adding the required files in order for the site to be built
a.	_quarto.yml
b.	Index.qmd
c.	styles.css (this file is empty but reference in the _quarto.yml)
d.	This files are not needed but use in the _quarto.yml for a png
i.	Images (folder)
3.	Adding a new tab to the portfolio. I’m adding a resume
a.	In the _quarto.yml file add, under the navbar, and this two lines of code
- text: "My Resume"
  file: resume.qmd
b.	Add/create the qmd file for your resume to the root folder
i.	Render the resume.qmd file
c.	Update yml links
i.	Build > render website
ii.	Or run this code in the console or terminal: quarto render --execute _quarto.yml
d.	Push to github and the site should be updated with your new tab.

Part 1.
1.	In your repository page, create a new repository
a.	Not using a template for this one
b.	Choose owner, for this one should just be you. 
c.	Name your repository
d.	Click on Add a README file and hit Create repository
e.	Only file currently is the README.md file
2.	Creating new project in R studio for your new repository
a.	On the main github page for your repository. Click on the green rectangle for code and copy the URL
b.	Create new project in R-studio
i.	Open up r studio, and create a new project
ii.	Click on Version Control - then on Git and paste the url in the Repository URL: section
iii.	Under Create project as subdirectory, make sure your path is in your hardrive. 
iv.	Create Project
c.	This steps should have created the .gitignore, Portfolio_template, and two normally hidden folders (.git and .Rproj.user [.Rproj.user folder (this doesn't affect your files, but clears RStudio's cache for the project).] )
i.	.gitignore settings
1.	The non-working project ignores files like .Rhistory, .RData, and .Ruserdata. These are harmless and irrelevant for website rendering or Build tab visibility.
2.	This is interesting to know this files are ignore because I use em all the time so it pays to research this. 
ii.	
Part 2
1.	Add the _quarto.yml, index.qmd and styles.css files need to build the website. 
a.	Other files can be added but this are the only ones needed for this template
i.	You can edit as much as you want here and add anything you want. I’m just showing what is required for this template to be built. Limit editing if unfamiliar with github pages. 
b.	Render Website
i.	Run this command in the console
1.	quarto::quarto_render()
2.	restart r studio. (this code can also be ran in an r chunk as well)
ii.	The goal of this command is to let r studio know this is a _site and gives the option to build site and render website (option next to git)
c.	Render the website using the build option in r studio
i.	After using the manual render site, github should now have an option to build > render website. 
1.	Render website 
quarto::quarto_render()

2.	Push to github
a.	Once you render the index file, push to github ( git add . ---- git commit -m”update” ---- git push)
b.	On the github repository, go to settings/pages and under branch
i.	Set Branch to main and set folder to /docs and hit save
1.	Once you hit save, github will know to deploy the site.
c.	If done correctly the site should be live. 


Part 3
Not to complicated


