---
title: "Getting Started with SharePoint Framework (SPFx)" # Title of the blog post.
date: 2022-04-27T00:00:00-04:00 # Date of post creation.
description: "Understanding what SharePoint Framework (SPFx) is and how to develop with it is important to be able to customize and expand your SharePoint capabilities." # Description used for search engine.
featured: false # Sets if post is a featured post, making appear on the home page side bar.
#draft: false # Sets whether to render this page. Draft of true will not be rendered.
#toc: false # Controls if a table of contents should be generated for first-level links automatically.
# menu: main
#usePageBundles: false # Set to true to group assets like images in the same folder as this post.
featureImage: "/images/blog/featured-getting-started-with-sharepoint-framework-spfx.jpg" # Sets featured image on blog post.
#featureImageAlt: 'Description of image' # Alternative text for featured image.
#featureImageCap: 'This is the featured image.' # Caption (optional).
thumbnail: "/images/blog/thumbnail-getting-started-with-sharepoint-framework-spfx.png" # Sets thumbnail image appearing inside card on homepage.
#shareImage: "/images/path/share.png" # Designate a separate image for social media sharing.
#codeMaxLines: 10 # Override global value for how many lines within a code block before auto-collapsing.
#codeLineNumbers: false # Override global value for showing of line numbers within code block.
#figurePositionShow: true # Override global value for showing the figure label.
redirectUrl: 'https://www.marathonus.com/about/blog/getting-started-with-sharepoint-framework-spfx/'
categories:
  - Getting Started
tags:
  - SharePoint
  - SPFx
  - ReactJS
  - Webpart
comment: false # Disable comment if false.
---

Back in 2016, Microsoft unveiled the next development model for SharePoint called the SharePoint Framework (SPFx). Over the years, SharePoint Framework has evolved from the ability to create just SharePoint Webpart into a sophisticated framework that includes Field Customizer, ListView Command Set, Microsoft Teams tab apps, and much more.

So, what is SharePoint Framework? Well, SharePoint Framework, better known as SPFx, is a client-side development framework that utilizes modern development toolchains to create web parts and solutions for SharePoint Online. Someone in the SharePoint community once called SPFx “a formal way of creating the JavaScript web parts without content editor web parts.”

Microsoft has even moved all their SharePoint development for SharePoint first-party web parts into SPFx. Unlike previous SharePoint development models, this one is here to stay!


## Component Types of SharePoint Framework
There are 4 main component types in SharePoint Framework that you can build: web parts, extensions, libraries, and Adaptive Card Extension.

### Web Parts
SharePoint web parts are display controls that can be put on almost any SharePoint page. Every site page within SharePoint has web parts on them, whether the page was built by you or Microsoft. With SharePoint Online, these web parts are all client-side and execute client-side in the browser.

### Extensions
SPFx extensions allow you to enhance the user experience within modern SharePoint pages, document libraries, or lists views. There are 3 types of extensions you can create:

- **Application Customizers:** This allows you to add functionality to all pages within SharePoint Online quickly. They can also be used to add custom HTML into the well-known SharePoint placeholders for a custom look and feel.
- **Field Customizers:** This allows you to modify views to data for fields within a list. This is the replacement for jsLink in classic SharePoint.
- **Command Sets:** This allows you to create custom buttons on modern SharePoint pages to create new actions and custom behaviors as needed.

### Libraries
The library component type allows you to share code and functions across multiple SharePoint Framework projects. They are deployed just like a web part but can be referenced in code like a shared DLL from full-trusted solutions from SharePoint On-Premises. 

### Adaptive Card Extension
The Adaptive Card Extension is new with the growth of Microsoft Viva. This component type enables developers to build extensions to Viva Connections' dashboards and SharePoint pages.

## Getting Started

What will you need to get started with developing your first SharePoint Framework solution?

First, install [Node.js](https://www.nodejs.org/). SharePoint Framework v1.14.0 is supported on the following Node.js versions:

- js v12.13.0+ (Erbium)
- js v14.15.0+ (Fermium)

Based on my experience, I would recommend starting with installing Node Version Manager (NVM). NVM is a tool used to install and run multiple versions of NodeJS on a machine. It allows you to switch between NodeJS versions based on the project you are working on on the same machine. NVM will allow you to fix issues in older projects (such as projects written with SPFx 1.10 and NodeJS v10) while working on new projects with SPFx 1.14.0 and NodeJS V14 without having to upgrade the older code to the newer version framework.

Note: at the time of this article, SharePoint 1.15.0 was just released in beta. We will be using SharePoint 1.14.0 for all the examples.

### Installing NVM
First, download the nvm-setup.zip from the project’s GitHub Repository and unzip/extract the file.

![NVM Assets](/images/blog/getting-started-with-sharepoint-framework-spfx/nvm-assets.png "NVM Assets")

Then, run the nvm-setup.exe file that was extracted from the zip file.

![NVM Zip File](/images/blog/getting-started-with-sharepoint-framework-spfx/nvm-zipfile.png "NVM Zip File")

Note: you may receive a User Account Control prompt when trying to run this executable.

Accept the license agreement and continue the installation with the defaults until the setup wizard is completed.

![NVM Command Line](/images/blog/getting-started-with-sharepoint-framework-spfx/nvm-commandline.png "NVM Command Line")

Finally, we need to install one of the NodeJS versions. Within the command prompt, run nvm install 14.19.0.

![NVM Install 14.19.0](/images/blog/getting-started-with-sharepoint-framework-spfx/nvm-install-14190.png "NVM Install 14.19.0")

Now, to select NodeJS v14 for use, run the following command. You may receive an access is denied error message. This is because you need to run the command prompt as an administrator.

![NVM Use Error](/images/blog/getting-started-with-sharepoint-framework-spfx/nvm-use-error.png "NVM Use Error")

After you open a new command prompt window as an administrator, run the command again and you will now be using Node v14.19.0.

![NVM Use Completed](/images/blog/getting-started-with-sharepoint-framework-spfx/nvm-use-completed.png "NVM Use Completed")

## Install the Development Toolchain

SharePoint Framework used common open-source tools such as Gulp and Yeoman. You will need to install both these tools plus the SharePoint Framework Yeoman Generator. The SharePoint Framework Yeoman Generator creates the initial structure of your SharePoint Framework project.

```bash
npm install gulp-cli yo @microsoft/generator-sharepoint@1.14.0 --global
```
![NVM Install](/images/blog/getting-started-with-sharepoint-framework-spfx/npm-install.png "NVM Install")

This will take a few minutes, but when it’s completed, you will have Gulp, Yeoman, and the SharePoint Framework Yeoman Generator installed on your machine.

![NVM Install](/images/blog/getting-started-with-sharepoint-framework-spfx/nvm-completed.png "NVM Completed")

## Creating Your First SPFx Web Part
Now it’s time to create your first SharePoint Framework web part.

You’re going to start by running the SharePoint Framework Yeoman Generator to create the file structure of your project. Look at this as the SharePoint project template in Visual Studio.
```bash
yo @microsoft/sharepoint
```
If this is the first time running a Yeoman Generator on this machine, it will ask if you are willing to send anonymous stats to improve the tool. Your choice is not going to impact your use of the tool, so pick what is best for you.

![Yo First Time](/images/blog/getting-started-with-sharepoint-framework-spfx/yo-first-time.png "Yo First Time")

When you get past that, the Yeoman Generator will ask you some questions on what you are building.

First, it will ask the name of your solution. Pick a name that is meaningful to you, as this is the name the build process will use to create the package file.

Second, it will ask what you are trying to create. There are several component options within the SharePoint Framework of what you can create. For this example we will be creating a web part.

![Yo Step 1](/images/blog/getting-started-with-sharepoint-framework-spfx/yo-spfx-1.png "Yo Step 1")

Next, it will ask you for the name of your web part. Don’t use the word “WebPart” in your name, as the generator will create the folder with WebPart in it twice.

Finally, the SPFx generator will ask you what template you would like to use. This is what JavaScript framework you want to use. When I started with SFPx, I used “No framework” and added jQuery to the project. At the time, jQuery was something I knew how to write, so it gave me a comfortable starting point. Now, after almost 6 years of working with SPFx, I go with React.

Choose the JavaScript framework you are comfortable with. There’s a lot to learn and understand with SharePoint Framework, so don’t add a new JavaScript framework to learn as well from the beginning.

![Yo Step 2](/images/blog/getting-started-with-sharepoint-framework-spfx/yo-spfx-2.png "Yo Step 2")

Now, sit back and let the SharePoint Framework Yeoman generator do its thing. It will first create the file structure and then it does the most important part: it installs the over 100 NodeJS packages needed for an SPFx project.

![Yo Step 3](/images/blog/getting-started-with-sharepoint-framework-spfx/yo-spfx-3.png "Yo Step 3")

There is one last command we need to run before we can check out the web part. From within the command prompt run:
```bash
gulp trust-dev-cert
```
![Gulp Trust Dev Cert](/images/blog/getting-started-with-sharepoint-framework-spfx/gulp-trust-dev-cert.png "Gulp Trust Dev Cert")

This creates a local certificate for you to be able to load your web part into SharePoint Online for testing and debugging.

![Gulp Trust Dev Cert Prompt](/images/blog/getting-started-with-sharepoint-framework-spfx/gulp-trust-dev-cert-prompt.png "Gulp Trust Dev Cert Prompt")

Once the SharePoint Framework Yeoman generator is completed and the local certificate is created, we are ready to check out the web part.

Open your code editor. In this example, I will be using Visual Studio Code.

![VS Code Files](/images/blog/getting-started-with-sharepoint-framework-spfx/vs-code-files.png "VS Code Files")

Before we see the web part on a SharePoint page, we need to edit one file first.

Under the config folder, open the serve.json file and edit the “intialPage” value in the Json with your SharePoint site. This can be any site within your SharePoint tenant.

![Serve Json File](/images/blog/getting-started-with-sharepoint-framework-spfx/servejson-file.png "Serve Json File")

![Edit Serve Json File](/images/blog/getting-started-with-sharepoint-framework-spfx/edit-servejson.png "Edit Serve Json File")

Now, run gulp serve in your command prompt.
![Gulp Serve](/images/blog/getting-started-with-sharepoint-framework-spfx/gulp-serve.png "Gulp Serve")

Your default browser will open directly to your SharePoint site’s workbench. The workbench is a location within every site where you can work on your web part without impacting a live page.

![Workbench Blank](/images/blog/getting-started-with-sharepoint-framework-spfx/workbench-blank.png "Workbench Blank")

Click on the plus icon on the page and select your web part.

![Workbench Add Webpart](/images/blog/getting-started-with-sharepoint-framework-spfx/workbench-add-webpart.png "Workbench Add Webpart")

You have now loaded your first SharePoint Framework web part on a page.

![Workbench Add Webpart](/images/blog/getting-started-with-sharepoint-framework-spfx/workbench-hello-world.png "Workbench Add Webpart")

## Important Gulp Commands
```bash
gulp trust-dev-cert
```
Creates a local certificate for development and debugging.
```bash
gulp serve
```
Creates a local webserver to host the client-side code of your solution.
```bash
gulp clean
```
Clears out all complied code from the release folder.
```bash
gulp build
```
Builds and compiles the JavaScript code within your project.
```bash
gulp build --ship
```
Builds and compiles the JavaScript code within your project for production use.
```bash
gulp bundle --ship
```
Bundles and minifies your JavaScript to optimize your files to reduce the number of server requests for JavaScript files.
```bash
gulp package-solution --ship
```
Creates the deployment package with all your JavaScript files and any other assets your project requires.

### Conclusion
Hopefully this article was useful in getting you started with your first SharePoint Framework web part. There is a lot you can do with the SharePoint Framework, such as single app pages and Microsoft Teams tabs. In future articles, I will go into more detail on how to do these and more.