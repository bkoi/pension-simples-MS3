Do you want to understand your pension better? Why not try **Pension Simples**, a straightforward and easy-to-use pensions jargon buster?

## Table of contents

> 1.  [Overview](#overview)
> 2.  [User Experience Design (UX)](#user-experience-design)
> 3.  [Features](#features)
> 4.  [Technologies Used](#technologies-used)
> 5.  [Testing](#testing)
> 6.  [Deployment](#deployment)
> 7.  [Credits](#credits)
> 8.  [Acknowledgements](#acknowledgements)

---
## Overview

**Pension Simples** is a glossary of pension terms that explains the terminology used in annual benefit statements, pension related documents or referred to during any interaction with a pension provider. As I work in this field, I truly understand why most people struggle to make sense of the jargon. I genuinely want to provide them with a resource that could be a game-changer as the compilation explains these terms in plain English. Understanding is key in getting the most out of one's pension because it helps with requesting the right type of information and making wise pension related decisions, which ultimately impact how much financial comfort people can enjoy in their retirement.

This project is for educational purposes only and has been created for the Data-centric Development module of Code Institute.

View deployed site on [Heroku](https://id.heroku.com/login).

---

## User Experience Design / UX

* ### User stories
    1. I want to search for pension terms on a user-friendly and intuitive website.
    2. I want definitions to be displayed in an alphabetical order.
    3. I not only want to be able to browse the site but also want to be able to submit a new word, update an already existing term or request removal of a definition if I don't find it useful.
    4. I want to be able to ask for help if I can't find the term I need clarification on.
    5. I want to be able to locate contact details for a financial adviser should I decide to request advice.
    6. I want to ensure that my suggestions, requests are handled in a professional and secure manner so I expect to be able to sign up, log into to the site to make use of its extra features.

* ### Design and Structure
    The website's primary goal is to provide an easily-searchable collection of pension terms. Its structure and design supports intuitive and seamless user experience. 
    
    Due to the small screen size of mobile and tablet devices, menu options are discoverable under the hamburger menu on these interfaces. However, desktop users have all menu options spread along the top right-hand side of the navbar.

    Unregistered users can look up pension related expressions without having to log in or sign up by using the search bar, strategically located at the top of the page. As the definitions take up a high percentage of the useful screen space, only desktop users can search for terms via the A-Z links displayed on the left side of the page.

    All users have the option to request help by using the "Need Help?" button and search for a financial adviser via the link to an external site, called [unbiased.co.uk](https://www.unbiased.co.uk/) which is a leading platform connecting people to professional advisers.

    Registered users have access to all aspects of CRUD operations, meaning that they can request addition, update and also deletion of definitions via a relevant form linked to the database, subject to moderator's approval. Their session automatically ends in 15 minutes so it saves them from having to log out of the site. This time interval should be sufficient to complete and submit their request form.

* ### Database
    **Pension Simples** utilizes a NoSQL document-based database built in MongoDB for storing user details and the actual pension definitions. Two collections, "User" and "Term" have been created whose structure are demontstrated below.

    #### Database Design
    MongoDB Object format examples:

    **Collection: users**<br>
    {<br>
    &nbsp;&nbsp;&nbsp;&nbsp;_id: unique-value,<br>
    &nbsp;&nbsp;&nbsp;&nbsp;name: "Ann Smith"<br>
    &nbsp;&nbsp;&nbsp;&nbsp;email: "ann@gmail.com",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;password : "Dr0pBox9",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;password : "beneficiary"<br>
    }
    
    **Collection: terms**<br>
    {<br>
    &nbsp;&nbsp;&nbsp;&nbsp;_id: unique-value,<br>
    &nbsp;&nbsp;&nbsp;&nbsp;term_name: "beneficiary"<br>
    &nbsp;&nbsp;&nbsp;&nbsp;definition: "It is someone who benefits        from your pension or annuity should you pass away.",<br>
    }
   
   Due to security reasons, dabase connection details used for development are stored in an env.py file, are not uploaded to GitHub so that database and connection details are not visible to users. In production these are stored in Heroku.

* ### Wireframes

    All wireframes were created in [Balsamiq](https://balsamiq.com/wireframes/desktop/docs/). 

    #### Main portal Wireframe - [View]
    #### Login/Signup Wireframe - [View]
    #### Remove Wireframe - [View]
    #### Update Wireframe - [View]
    #### Add Wireframe - [View]


* ### Color Scheme
    To create a professional impression of the user interface, a monochrome [color palette](/static/img/color_palette.jpg) was chosen which incorporates different shades of blue.

    The background color is #f1f1f0.

    The main text color is #091d36.

    Buttons and elements with highlights use #5e83ba.
    
* ### Typography
    Roboto is well-known for its clear, geometric design with friendly an open curves, which makes it ideal to be used on a professional website aiming to make users feel more comfortable about a very often avoided part of their financial planning and well-being.
        
---
## Features
### Existing Features
* Home page providing information on the site's purpose.
* Sign up functionality.
* Sign in functionality.
* Automatic log out functionality after 15 minutes 
* Browser to search for pension terms.
* A-Z index with links to a section enlisting terms starting with the same letter of the alphabet
* Create term form for users to get their own definition added to the database and compilation
* Update term form for users looking to suggest a minor amendment to an existing expression
* Remove term form if a current term is found unhelpful for users
* "Need Help?" button with link to Contact form
* Link to an external site unbiased.co.uk for users looking for a financial adviser
* Mobile responsive design.

### Features Left to Implement
* Upvote and downvote option with counter
* Save, bookmark terms
* Printer functionality to print off the terms bookmarked by users
* Sharing terms with others via standard social media links
* Quick scroll-up "Top" functionality

---
## Technologies Used


* [HTML](https://en.wikipedia.org/wiki/HTML5)
* [CSS](https://en.wikipedia.org/wiki/CSS)
* [JavaScript](https://en.wikipedia.org/wiki/JavaScript)
* [Python](https://www.python.org/)
* [MongoDB](https://www.mongodb.com/)
  MongoDB served as the document-based database for this project.
* [Bootstrap:](https://getbootstrap.com/docs/4.6/getting-started/introduction) 
    Bootstrap was used to enable the responsiveness and assist with the styling of the website.
* [jQuery:](https://jquery.com/)
    jQuery was part of the Bootstrap bundle and was incorporated in order to make the navbar responsive.
* [Balsamiq:](https://balsamiq.com/wireframes/)
    Balsamiq was used to create the wireframes for the design before implementing them.
* [Google Fonts:](https://fonts.google.com/)
    Google Fonts provided the inspiration for my font choices.
* [Git:](https://git-scm.com/)
    Version control was maintained by applying Git via the Gitpod terminal to commit to Git and push the source code to GitHub.
* [GitPod:](https://www.gitpod.io/)
    The GitPod environment was used to develop the code before committing and pushing it to GitHub.
* [GitHub:](https://github.com/)
    The GitHub repository stores the project's source code.
* [Heroku](https://dashboard.heroku.com/apps)
    Heroku was used to deploy the live website.

---
## Testing

### Validator Testing
* HTML validation via [W3C Markup Validator](https://jigsaw.w3.org/css-validator/#validate_by_input) - [Results]()
* CSS validation via [W3C CS Validator](https://jigsaw.w3.org/css-validator/#validate_by_input) - [Results]()
* JavaScript validation via [JSHint](https://jshint.com/) - [Results]()
* Python validation via [PEP8 Validator](http://pep8online.com/)

### Testing User stories from User Experience Section
* #### User Goals

The webpage was extensively tested on various devices and browsers. Any bugs related to these are noted in the **Bugs** section.

### Bugs

### Unfixed Bugs
---
## Deployment

### GitHub Pages
The site was deployed to GitHub pages. The steps to deploy are as follows:

1. Navigate to the repository on GitHub, then click **Settings**.
1. Click **Pages** in the left sidebar.
1. Under **GitHub Pages - Source** select the **Branch: master** drop-down menu and select a publishing source, then click **Save**.
1. The live website is available at <!---->
1. Any commits are pushed to GitHub which ensures that the GitHub Pages version gets updated in a timely manner.

### Making a Local Clone

1. On GitHub navigate to the main repository, click **Code**.
1. From the **Clone** options, use the **HTTPS** option and copy the link displayed.
1. Open your IDE and ensure you have a Git Terminal open.
1. Change the current working directory to the location where you want the cloned directory.
1. Type ```git clone```, then paste the URL you copied earlier.
1. Press **Enter** to create your local clone.

### Project Creation
To create this project I used the CI Gitpod Full Template by navigating 
[here](https://github.com/Code-Institute-Org/gitpod-full-template) and clicking the 'Use this template' button.

I was then directed to the create new repository from template page and entered in my desired repo name, then 
clicked Create repository from template button.

Once created, I navigated to my new repository on GitHub and clicked the Gitpod button which built my workspace.

The following commands were used for version control throughout the project:

* git add *filename* - This command was used to add files to the staging area before committing.

* git commit -m "commit message explaining the updates" - This command was used to to commit changes to the local repository.

* git push - This command is used to push all committed changes to the GitHub repository.


### Deployment to Heroku

*Create application:*
1. Google Heroku.com and login.
1. Click on the "New" button.
1. Select "Create new app".
1. Enter the app name.
1. Select region.

*Set up connection to Github Repository:*

1. Click the "Deploy" tab and select "GitHub" to connect to GitHub.
1. Under "App connected to GitHub" enter your repository name, then click "Search".
1. Once your repo is found, click the "Connect" button.

*Set environment variables:*

Click the "Settings" tab, then click the "Reveal Config Vars" button to add the following:

1. key: IP, value: 0.0.0.0
2. key: PORT, value: 5000
3. key: MONGO_DBNAME, value: (database name you want to connect to)
4. key: MONGO_URI, value: (mongo uri - This can be found in MongoDB by going to clusters > connect > connect to your application and substituting the password and 
    dbname that you set up in the link).
5. key: SECRET_KEY, value: (This is a custom secret key set up for configuration to keep client-side sessions secure).

*Enable automatic deployment:*
1. Click the "Deploy" tab
1. In the "Automatic deploys" section, choose the branch you want to deploy from then click "Enable Automation Deploys".

*Run Locally*

You will only be able to run the app locally with being connected to a database if the [env.py](https://pypi.org/project/env.py/) file contains the configuration for IP, PORT,  MONGO_URI, MONGO_DBNAME and SECRET_KEY. You must have the connection details in order to do this. These details are private and not disclosed in this repository 
for security purposes.

1. Go to the GitHub [Repository](https://github.com/bkoi/pension-simples-MS3).
1. Click the "Code" drop down menu next to the Green Gitpod button.
1. You can either "Download ZIP" file, unpackage locally and open with GitHub Desktop(with no more steps) OR Copy Git URL from the "HTTPS" dialogue box.
1. Open your development editor of choice and open a terminal window in a directory of your choice.
1. Use the 'git clone' command in terminal followed by the copied git URL.
1. A clone of the project will be created locally on your machine.

Once the project has been loaded into an IDE of choice, run the following command in the shell to install all the required packages:
> pip install -r requirements.txt

### Fork Project 

If you like this project and would like to use it as a starting point or want to make changes to it you can fork it. 

1. Navigate to the GitHub Repository you want to fork.
1. On the top right of the page under the header, click the "Fork" button.
1. This will create a duplicate of the full project in your GitHub Repository.

---
## Credits

### Content
I have utilisew some of the structural design of [Daisy McGirr's](https://github.com/Daisy-McG/Motorbike-Event-Finder) README and copied her deployment steps.


### Design
Color palette inspiration: 
https://colorpalettes.net/color-palette-2326/

## Acknowledgements

I would like to thank my Mentor, Ronan McClelland for his helpful feedback, and also the Slack community who had dealt with the same issues that I encountered during the development of this project. It was tremendously useful to have access to their previous challenges and their solutions.



