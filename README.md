# Artsy Engineering Team Onboarding

Welcome to Artsy! If you're not an Artsy team member we hope you'll find these docs useful and maybe check out our [jobs](https://www.artsy.net/jobs) or just send us a resume to [jobs@artsy.net](mailto:jobs@artsy.net).

If you're a new team member, we’re excited to have you!

Before you begin this guide, keep in mind that it is a work in progress and your first PR at Artsy could be fixing a typo/adding more information to [this doc](https://github.com/artsy/potential/blob/master/README.md). This will guide you through some basic readings/tasks to get you started engineering @Artsy. If you have questions feel free to reach out to your mentor or anyone else on the dev team. Try the #dev channel on Slack.

Whether you're a seasoned engineer or fresh out of school, take a moment to read [Your First 60 Days at an Engineering Job](http://code.dblock.org/2015/04/23/your-first-60-days-at-an-engineering-job.html).

## Overview

### Administrivia

#### Onboarding

You have been onboarded by ops. You have a mentor and a spirit guide. You now know where we keep the snacks! Awesome.

##### 1Password + Dropbox

Download and install Dropbox and 1Password and configure 1Password vaults as described [in this guide](dropbox-1password/dropbox-1password.md).

##### Slack

Download and install Slack, see [this guide](slack/slack.md) for details.

##### Trello

Each team does task management slightly differently, but in general we use [Trello](https://trello.com) for high-level tasks and github issues for project-level tasks. Ask your mentor to get you signed up and subscribed to the relevant Trello boards.

##### GitHub

Artsy keeps all of our code on [GitHub](https://github.com/artsy). Make sure you have a GitHub account and are part of the Artsy Engineering organization. If you can’t visit [this page](https://github.com/artsy/gravity), then you don’t have the right access. Your mentor can get you sorted out.

You’ll notice that our GitHub repos are named after physics terms. The story is that our first project, gravity, was named after [Zachary Coffin's "Temple of Gravity"](http://www.zacharycoffin.com/work/temple-of-gravity) that was installed at Burning Man in 2003. The work weighs 180,000 lbs total and involves walking under 17,000 lbs stones swinging from two apparently insubstantial chains. In 2011 we wanted to build a brand new, rock solid foundation for Artsy platform and chose The Temple of Gravity for its art + science metaphor.

![](images/gravity.jpg "Gravity")

_"Gravity cannot be held responsible for people falling in love.", - Einstein_

See the [engineering projects map](https://trello.com/b/VLlTIM7l/artsy-engineering-projects-map) for an in-depth look at our (many) repos and who owns them. It can be a bit overwhelming, so here is a breakdown of a few important ones:

* [Gravity](https://github.com/artsy/gravity): Artsy’s API
* [Force](https://github.com/artsy/force): Artsy desktop website (www.artsy.net)
* [MicroGravity](https://github.com/artsy/microgravity): Artsy mobile website (m.artsy.net)
* [Eigen](https://github.com/artsy/eigen): Artsy mobile app
* [Volt](https://github.com/artsy/volt): Artsy CMS for partners
* [Torque](https://github.com/artsy/torque): Artsy main admin app (user management, etc.)

##### AWS

In order to get applications like Gravity set up, you’ll need the proper AWS credentials. Ask your mentor to give these to you as well.

We use [AWS](https://artsy.signin.aws.amazon.com/console) for storage (S3), hosting websites (OpsWorks), and analytics (Redshift), among other things.

##### Art world notes

Many of our engineers have art backgrounds or degrees, but of course not all of them. [Here](art/resources.md) are some useful links if you want to read more about the art world, or keep up with the latest news.

### Artsy Engineering Operations

##### The Artsy Product & Engineering Teams

Artsy product engineering is organized in product teams. Each team has a _purpose_, eg. _"Help galleries get the most out of Artsy and run their business better"_, and Key Performance Indicators, or KPIs, eg. _"The number of artworks uploaded by partners."_ Each team has members with different responsibilities, including a _Product Lead_, a _Project Manager_, a _Designer_, an _Engineering Lead_ or an _Engineer_, depending on size. Sometimes the same person wears multiple hats.

You can see this organization [live in the Product and Engineering Teams Trello](https://trello.com/b/Ws7rgCUU/product-and-engineering-teams).

Engineers typically work on a product team and belong to an _Engineering Practice_.

* Platform Practice
    - Team lead: [Joey](https://github.com/joeyAghion) [joey.aghion.com](http://joey.aghion.com)
    - Slack: [#platform-humans](https://artsy.slack.com/messages/platform-humans)
    - [Platform Practice Overview](platform/README.md)
* Mobile Practice
    - Team lead: [Orta](https://github.com/orta) [orta.io](http://orta.io)
    - Slack: [#mobile](https://artsy.slack.com/messages/mobile)
    - [Mobile Practice Playbook](mobile/mobile.md)
* Web Practice
    - Team lead: [Craig](https://github.com/craigspaeth) [craigspaeth.com](http://craigspaeth.com)
    - Slack: [#web](https://artsy.slack.com/messages/web)
    - [Web Practice Playbook](web/web.md)

##### Engineering Team Standup

We have an engineering team-wide standup on *Mondays at 2 p.m.* where we give a high-level overview of what we worked on the previous week and what we hope to accomplish in the coming week.

##### Open Source Culture + Projects

At Artsy, we <3 open source and encourage you to become part of the community. Here is a [list of some open source technologies](http://artsy.github.io/open-source/) we currently use.

Read dB.’s blog post on [Becoming Open Source by Default](http://code.dblock.org/2015/02/09/becoming-open-source-by-default.html).

Read this [article by the mobile team](http://www.objc.io/issue-22/artsy.html) on the culture of open source at Artsy and their reasons behind open-sourcing our [mobile app](https://github.com/artsy/eigen).

Orta also wrote a blog post on the [mechanics behind open-sourcing Eigen](http://artsy.github.io/blog/2015/04/28/how-we-open-sourced-eigen/).

##### The Artsy Stack

This blog post by dB. explains [our stack, circa 2015](http://artsy.github.io/blog/2015/03/23/artsy-technology-stack-2015/).

## Setting up your Dev Environment

Many of these are adopted from Joey’s gist: [How Joey Works](https://gist.github.com/joeyAghion/02dcf1d40829731525fb)

### Getting ready to Code

##### Text Editor

Most Artsy Engineers use [Sublime Text 2](http://www.sublimetext.com/2), but feel free to use whatever makes you most comfortable.

You can use the [Sublime Package Manager](https://packagecontrol.io/installation) to manage plugins in Sublime.

Once you have Package Manager installed, packages can be installed by following the [instructions here](https://packagecontrol.io/docs/usage). It all starts with `cmd+shift+p`.

If you do use Sublime, here are some plugins you might want to get you started:

* [Git](https://packagecontrol.io/packages/Git)
* [GitGutter](https://github.com/jisaacks/GitGutter)
* [GitHubinator](https://packagecontrol.io/packages/GitHubinator)
* [Markdown preview](https://github.com/revolunet/sublimetext-markdown-preview) or [OmniMarkupPreviewer](https://packagecontrol.io/packages/OmniMarkupPreviewer)

### Making Contributions

As all of our code is housed on GitHub, we make contributions through [pull requests](http://artsy.github.io/blog/2012/01/29/how-art-dot-sy-uses-github-to-build-art-dot-sy/).

Read about our workflow [here](github/workflow.md).

If you are unfamiliar with Git, check out this [short tutorial](https://try.github.io) on basic git commands (such as `git status`, `git commit`, and `git push`).

If you'd like a more comprehensive review of Git and GitHub and how we use them, you can look at our Guide to [Git and GitHub](github/git_and_github.md).

##### Style Guide

For a more indepth guide to our contribution workflow and our style preferences for Git and Pull Requests, you can view our [Style Guide](github/style_guide.md).

The GitHub blog also has a nice article on [writing quality pull requests](https://github.com/blog/1943-how-to-write-the-perfect-pull-request).

### Deploying Software

Once your pull request is merged, we use services like [Semaphore](https://semaphoreci.com/) and [Travis](https://magnum.travis-ci.com/) to run a full build of the app to make sure the code changes did not break existing features.

Most of our apps do not automatically deploy once the CI (continuous integration) step succeeds. Instead, you have to manually deploy the code to where it's hosted (usually either [Heroku](https://dashboard.heroku.com/) or [OpsWorks](https://console.aws.amazon.com/opsworks/home)). This process is app-specific, but generally done through the [Jenkins](http://joe.artsy.net:9000/) or Semaphore UI, or the command line.

We don't have a set deployment cycle for our web apps (developing for iOS is a different story...). At Artsy, we value small improvements through pull requests, and incremental deploys. You don't need permission to deploy-- you just have to announce when you plan to deploy something in the relevant slack channel in case someone is intentionally putting it off.

Our API app, Gravity, is hosted on OpsWorks. For more information on why we chose OpsWorks for this app, and *what it all means*, check out our [Introduction to AWS OpsWorks](http://artsy.github.io/blog/2013/08/27/introduction-to-aws-opsworks/) blog post.

## If You Get Stuck

#### Slack

If you know what team could potentially help you, browse the channels in Slack to find the most relevant place to ask your question. If you aren't sure, [#dev](https://artsy.slack.com/messages/dev) is a good place to start.

#### Ask Your Neighbor

Everyone is really friendly - don't hesitate to reach out to the people around you for even the most basic of questions.

### License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Artsy Potential</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://artsy.net" property="cc:attributionName" rel="cc:attributionURL">Artsy</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/artsy/potential" rel="dct:source">https://github.com/artsy/potential</a>.
