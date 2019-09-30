# Stack

This is a static site that is generated using Hugo.
Hugo requires Go v1.11 to be installed
https://gohugo.io/

It is automatically deployed by Netlify 
https://www.netlify.com/

To
https://sleepy-wilson-e5c9f4.netlify.com/


# Recommended Set up

## Install an IDE that has a terminal window
Like Visual Studio Code
https://code.visualstudio.com/download

## Install Go
Open terminal in VSCode and check if Go is installed by typing 'go version'
if not installed or version is lower than 1.11, install Go
https://golang.org/dl/

## Install Hugo
On a mac you can brew install hugo

Outside of a mac, the fastest way is to clone hugo and build hugo locally
Hugo uses go modules support built into Go 1.11 so clone it to a directory outside the go path then go install it. 

git clone https://github.com/gohugoio/hugo.git
cd hugo
go install --tags extended

## Clone the site
Git clone the site to your local machine
The sites theme is a git submodule so will need to add --recurse-submodules when cloning it. 
Example command to clone it would be
git clone git@github.com:geordietestatelier/site.git --recurse-submodules


## Run the site locally
in the root folder type: 
hugo server
Then either click the link in the terminal window or navigate to http://localhost:1313/ in a browser
You will see the site, any changes you make to the code will update in real time in this browser window

## Changing the site
The data folder has some of the content stored there in yaml files that configure the widgets on the page.
The blog posts live in /content/blog
If you want to change a specific bit of text then the following command
git grep -n "the text you want to change"
should tell you where to find that text

## Building and Deploying
After making changes, type 'hugo'
this is the command to rebuild the static site with your changes.

git commit and git push changes to master
if you log in to netlify with the geordietestatelier GitHub credentials you will be able to see the site building and deploying. It usually takes about 30 seconds to deploy.

Site changes are now live at https://sleepy-wilson-e5c9f4.netlify.com/

