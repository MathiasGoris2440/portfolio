---
title: "Creating My Personal Website with Hugo and Netlify"
date: 2024-04-20T22:53:58+05:30
draft: false
author: "Mathias Goris"
tags:
  - Hugo
  - Netlify
  - GitHub
  - Website Development
image: /images/hugo-logo.jpg
description: "A step-by-step guide on how I built and deployed my personal website using Hugo, GitHub, and Netlify."
toc: 
---
Creating a personal website has never been easier with the plethora of tools available today. In this blog post, I’ll walk you through how I built my website using Hugo, a fast and flexible static site generator, and the Hugo Profile theme. I then hosted my website on Netlify using GitHub for version control.

## Choosing Hugo and the Hugo Profile Theme

I chose Hugo because of its speed and ease of use. It allows you to create static websites quickly with simple configuration and extensive documentation.

### Installing Hugo

To get started, I installed Hugo on my machine. You can follow the [official installation guide](https://gohugo.io/getting-started/installing/) for your operating system.

```bash
brew install hugo
```

## Setting Up the Hugo Profile Theme
Once Hugo was installed, I created a new site and added the Hugo Profile theme.

```bash
hugo new site my-website
cd my-website
git init
git submodule add https://github.com/gurusabarish/hugo-profile.git themes/hugo-profile
```

I then copied the example content to get started quickly:

```bash
cp -r themes/hugo-profile/exampleSite/* .

```

## Customizing the Website

With the basic setup done, I customized the content and configuration to make the website my own. This involved editing the config.yaml file and adding my personal information, social links, and content.

## Editing the Configuration

I opened the config.yaml file and made changes to reflect my personal details and preferences. Here’s a snippet of my configuration:

```bash
baseURL = "https://yourdomain.com/"
languageCode = "en-us"
title = "Mathias Goris"
theme = "hugo-profile"

[params]
  author = "Mathias Goris"
  description = "Personal website and blog"
  # Other parameters...

```

## Adding Content

I added my own content by creating new markdown files in the content directory. For example, to add a new blog post:

```bash
hugo new posts/my-first-post.md
```

I then edited the markdown file to add my content.

### Hosting on Netlify

With my website ready, the next step was to deploy it. I chose Netlify for its seamless integration with GitHub and ease of use.

## Pushing to GitHub

First, I pushed my Hugo site to a GitHub repository.

```bash
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/username/my-website.git
git push -u origin master
```

## Setting Up Netlify

I created an account on Netlify and connected it to my GitHub repository. Here’s how:

Go to the Netlify dashboard and click on “New site from Git.”
Select GitHub and authorize Netlify to access your repositories.
Choose the repository that contains your Hugo site.
Configure the build settings:
Build command: hugo
Publish directory: public
Click on “Deploy site.”

Netlify automatically builds and deploys your site. Any changes pushed to the GitHub repository will trigger a new build and deploy, keeping your website up to date.

### Conclusion

Building and deploying a personal website with Hugo, GitHub, and Netlify is a straightforward process. Hugo provides a powerful yet easy-to-use framework for creating static websites, and Netlify offers seamless deployment with continuous integration. Now, my website is live and easy to update with new content and features. Check it out at yourdomain.com!

Feel free to reach out if you have any questions or need help setting up your own website!
