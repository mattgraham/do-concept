---
layout: home
---

Great project. Although not a difficult "design" project, it is one that can add and subtract to the users success and thus the bottom dollar.

I have several thoughts on what I would change (along with some UX, SCSS and Markup), so I've created both this write up and a demo with code following. I look forward to talking through the process with you. Some very exciting challenges you have at DigitalOcean.


# Who is the user?

To understand how to best create the user experience you have to first make assumptions about the user. In most of our industry you find two major categories of users that are setting up servers:

- GUI Loving' Design and Development individuals
- Command Line Pro's

I'd like to break down these users to explain my ideas better.

## GUI Loving' Design and Development individuals

I believe this is the current target and I enjoy the flat consistent branding throughout the site however, there are a few things I'd change.

- Navigation
- Question lead experience / Order of Events
- Application Builds

### Navigation

I feel a bit crowded and confused by the navigation on the droplet creation page. I have several times (previous to us talking) wanted to click the create button on the left (again) to complete the build process:

![]({{ "/assets/images/writeup/demo-0.png" }})

It feels 'in the way' more often than not. I'd like to expand the creation page to take up the majority of the browser width and move the navigation to a fixed, collapsed position on the left of the site opening on hover.

![]({{ "assets/images/writeup/demo-2.gif" }})

I feel this continues to give quick access to the reset of the navigation items while keeping the 'web app' like experience.

### Question lead experience / Order of Events

This is what majority of my brain power was focused on. In conversation with Jesse I mentioned that I had a wordpress install installed on DigitalOcean and mentioned that I was using the $5 server unit. The response was, if we had talked you would have told me to use the $10 server. I would have made that change, had I have known.

I would change the build process to ask the questions in the order that can help DigitalOcean 'recommend' the right server.

**I would like to flip the current model upside down and add a few questions**.

In my model you would start with the OS Distribution, and even more so with the 'App' that you'd like to build. Having an application library (which I'm sure you are building and rebuilding often already) that is searchable creates great value.

- Hubot instance? 55 Seconds or Less.
- Jenkins integration server a minute from now? No problem.

The only other change other than order I can see being of value is the 'anticipated traffic' option. In honestly, its most likely a stronger marketing tool and justification tool for upselling the build, however, having the correct build upfront makes the upgrade process much easier.

## Command Line Pro's

One of the things I love the most about Heroku development setup is the quick and simple command line tool that not only sets up the server but also detects the technology used on pushing the app. DigitalOcean is not Heroku, nor, do we want it to be; however, I think there are tools and concepts we can use to make it a faster process for the command line user.

### Introducing the Digital Ocean Command Kit

What if there was a command line tool that setup the server via js file and then when command is run it builds in 55 seconds or less and deploys the code.

Something like `droplet setup` would create (after the user was logged in) a 'droplet' file in the root of the project folder; a file that would hold all the needed information to 'create' and new server. A 'power user' would then have these files preset for each client / server they setup. It would easily be modifiable via either text editor or the web interface.

<pre><code>{
  "name": "droplet-name",
  "size": "1gb",
  "region": "nyc2",
  "image": {
    "application": "LAMP",
    "distro": "ubuntu",
    "version": "14.04"
  },
  "settings": [
    "private-networking",
    "backups",
    "user-data"
  ]
}
</code></pre>

Then `droplet deploy` would run the setup process, toss errors and successes and build the server.

It would be incredible for it to 'recognize' that wordpress is in the project directory and ask if you wanted to add the application; however baby steps.

This would be the ideal answer to your question, How should a user create a droplet, if you were a command line junkie.


# Concept Preview

So that you can visually see some of the updates and code I've posted the app (on a DigitalOcean LAMP install no less). Some things to keep in mind:

- This is without question a prototype. I have not spent time browser testing, it is not responsive and the js and logic behind the form is 'display purposes only'
- Navigation icons are all svgs, the icons for the apps are a typeface. This is something that could be turned into one font for the entire site depending on the size differences of the assets.
- The tabs 'change' but do not change. My goal was to show the module, and a concept for the searching through the pre-built applications with their add on options.

Without further delay:

<a href="/demo.html" class="button">View Demo</a>

Assets were created in sketchapp
![](/assets/images/writeup/demo-3.png)

Complete design preview
![](/assets/images/writeup/Desktop_HD.png)

I have also invited your github account to the repo. The site is built initally in Jekyll and can be run locally with a few terminal commands.
