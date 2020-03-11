---
title: "WOD: Hard Rock Cafe (Meteor Version)"
published: false
morea_id: wod-hardrock-meteor-rtn
morea_type: experience
morea_summary: "Test your knowledge of Meteor" 
morea_sort_order: 1
morea_labels:
---

# WOD: Hard Rock Cafe (Meteor Version)

[The Honolulu Hard Rock Cafe](http://www.hardrock.com/cafes/honolulu/) is a popular local music venue. For this WOD, you will create a Meteor application based upon their home page. When completed, it should look like this (click on image to see full size):

{% include medium-img.html url="wod-1-hardrock-meteor.png" %}

Note that you will find your code from [Experience Island Snow Meteor](experience-meteor-islandsnow.html) to be very helpful.

Here are the steps:

## Step 0: Download the React mockup sources

Please download the [React HardRock Mockup Source](wod-1-hardrock-react.zip) zip file. Uncompress it to obtain the source files for this experience. 

## Step 1: Setup your repo with the template

Create a private GitHub repo called "hardrock-meteor", and check the box to initialize it with a README.
  
Clone it to your local file space.
  
cd into your local hardrock-meteor directory.
  
Download a zip file of [meteor-application-template-react](https://ics-software-engineering.github.io/meteor-application-template-react/) and uncompress it someplace other than your hardrock-meteor directory.
  
Copy the app/ directory, the config/ directory, and the .gitignore file into your hardrock-meteor directory. 
  
cd into the app/ directory, run `meteor npm install` and `meteor npm run start` to run the app. Go to [http://localhost:3000](http://localhost:3000) to see the app.
 
Now commit and push your repo to GitHub with the message "Template installed".  It should look like this:

## Step 2: Setup IntelliJ and ESLint

Create an IntelliJ project called "hardrock-meteor" that points to your repo.
  
Make sure that ESLint is configured correctly.  Open a Javascript file such as imports/startup/client/startup.jsx. ESLint might complain "Error: Failed to load plugin meteor: Cannot find module 'eslint-plugin-meteor'. Don't worry: just click the "ESLint Settings" link  and change the "ESLint Package" to the path to ESLint inside this project's node_modules directory. (In my IntelliJ, just pulling down the menu shows that path as an option). Once you select the correct path to ESLint, the error should disappear.  
  
To test that ESLint is working, add 3-4 blank lines to the bottom of the file. An ESLint error should now be displayed in the right margin in red.  Now delete them, and a green checkmark should reappear. (If it doesn't reappear immediately, then click on the red circle in the upper right side of the window, which should force re-inspection and generate the green checkmark.)
  
## Step 3: Port the Hard Rock React mockup to Meteor

Create a hardrock-react project in IntelliJ so that you have easy access to the React mockup source files that you downloaded in Step 0.

#### 3.1 Port the style.css definitions 
  
Port the global CSS classes by copying the contents of src/style.css (from the hardrock-react project) into app/client/style.css.

#### 3.2 Port the page components

Similar to the Island Snow experience, port the three page components (TopMenu, Middle, and Bottom) to the imports/ui/components directory.

#### 3.3 Port the page definition

Similar to the Island Snow Experience, port the HardRock component to the imports/ui/page directory.

#### 3.4 Make http:/localhost:3000/ point to the HardRock page

Now that we have an HardRock page, change the App component to route to HardRock instead of Landing when the path is "/".  You'll need to fix the imports.

Almost perfect, except that we are still displaying the NavBar and the Footer from meteor-application-template! 

#### 3.5 Fix the NavBar and the Footer

To fix the NavBar, remove the invocation of the TopMenu component inside the hardrock page, and replace the invocation of NavBar in the App layout with an invocation of TopMenu. Now "TopMenu" will appear by default at the top of every page.

Similarly, remove the invocation of Bottom inside the HardRock page, and replace the invocation of Footer in the App layout with an invocation of Bottom.  Now "Bottom" will appear by default at the bottom of every page. 

#### 3.5 Fix the title

In the last screenshot, notice that the Chrome tab for the page says "meteor-application-template".  To fix that, go to app/client/main.html, and change the title element text to "Hard Rock Cafe".  

## Step 4: Clean up the UI code

The last step is to remove the components and pages that you no longer need from your app.  For now, we'll just clean up the UI side of the system.  

First, though, commit and push your code to GitHub! 

Now, go through imports/ui/pages and imports/ui/components and delete the files associated with the template pages. If you make a mistake and the application breaks, you can simply go into GitHub Desktop and undo your mistake by right-clicking on the problematic file and selecting "Discard changes".

When you've deleted the template pages and components, commit and push your code to GitHub with the message "Completed Hard Rock Meteor Mockup".

## Task 5: Finish

When you can preview your application and it looks equivalent to the screen image above, commit and push your repo to GitHub.
  
Check to make sure it is present on GitHub.

Raise your hand to indicate you are done with this WOD.

{% include wod-times.html Rx="<40 min" Av="40-50min" Sd="50-60 min" DNF="60+ min" %}

### Submission instructions

{% include wod-submission-github.html assignment="Meteor WOD" %}

{% include goo.gl.html url="" %}










