# Artsy Engineering Team Onboarding

Welcome to Artsy! We’re excited to have you. Before you begin this guide, keep in mind that it is a work in progress and your first PR at Artsy could be fixing a typo/adding more information to this doc.

This will guide you through some basic readings/tasks to get you started engineering @Artsy. If you have questions feel free to reach out to your mentor or anyone else on the dev team.

Whether you're a seasoned engineer or fresh out of school, read dB’s short blog post [Your first 60 days at an engineering job](http://code.dblock.org/2015/04/23/your-first-60-days-at-an-engineering-job.html).

## Information, etc.

### Administrativa

##### 1Password
Ask dB for access to the Artsy Engineering 1Password Vault. You'll need to have this set up in order to access many of the services we use.

##### Slack
If you haven’t already, get on [Slack](https://artsy.slack.com/). You can download it from the [Apple store](https://itunes.apple.com/us/app/slack/id803453959?mt=12). We use Slack for all internal messaging, and prefer it to email in basically all cases.

Slack channels for every engineer to join:
* [#dev](https://artsy.slack.com/messages/dev): For asking questions to all engineers, or discussing things related to the dev team as a whole.
* [#dev-offtopic](https://artsy.slack.com/messages/dev-offtopic): Random things you want to send to the dev team that are not specifically work-related.
* [#help](https://artsy.slack.com/messages/help): For asking and answering questions.

A couple of Slack protocols/tricks:
* Typing `@channel` in any channel will send a notification to everyone in that channel. Refrain from doing this unless it’s imperative that everyone see your message. You can also `@` people directly in a channel, or direct-message them.
* `/hangout` starts a google hangout in that channel
* Slack uses markdown for styling text.
    - \`\`\````multi-line code```\`\`\`
    - \``single-line code`\`
    - \**italic*\*
    - \*\***bold**\*\*
* Read this short article on [getting the most out of Slack](https://medium.com/@slackhq/11-useful-tips-for-getting-the-most-of-slack-5dfb3d1af77)

##### Trello
Each team does task management slightly differently, but in general we use [Trello](https://trello.com/) for high-level tasks and github issues for project-level tasks. Ask your mentor to get you signed up and subscribed to the relevant Trello boards.

##### Github
Artsy keeps all of our code on [Github](https://github.com/artsy/). Make sure you have a Github account and are part of the Artsy Engineering organization. If you can’t visit [this page](https://github.com/artsy/gravity), then you don’t have the right access. Your mentor can get you sorted out.

You’ll notice that our Github repos are named after physics terms. Ask dB if you want to know why.

See the [engineering projects map](https://trello.com/b/VLlTIM7l/artsy-engineering-projects-map) for an in-depth look at our (many) repos and who owns them. It can be a bit overwhelming, so here’s a breakdown of a few important ones:
* [Gravity](https://github.com/artsy/gravity): Artsy’s API
* [Force](https://github.com/artsy/force): Artsy desktop website (artsy.net)
* [MicroGravity](https://github.com/artsy/microgravity): Artsy mobile website
* [Eigen](https://github.com/artsy/eigen): Artsy mobile app
* [Volt](https://github.com/artsy/volt): Artsy CMS for partners
* [Torque](https://github.com/artsy/torque): Artsy main admin app (user management, etc.)

##### AWS
In order to get things like Gravity set up, you’ll need the proper AWS credentials. Ask your mentor to give these to you as well.

We use [AWS](https://artsy.signin.aws.amazon.com/console) for storage (S3), hosting websites (OpsWorks), and analytics (Redshift), among other things.

### Artsy Engineering Operations

##### The Artsy Team
See [Carter’s email from the fall](https://groups.google.com/a/artsymail.com/forum/?hl=en#!searchin/team/update$20on$20product/team/YxDV2RrK56E/I3TbkjAhj1gJ) on how our product teams are structured.

Artsy engineering is broken up into four major teams:
* Platform
    - Team lead: Joey
    - Slack: [#platform-humans](https://artsy.slack.com/messages/platform-humans)
* Mobile
    - Team lead: Orta
    - Slack: [#mobile](https://artsy.slack.com/messages/mobile)
* Web
    - Team lead: Craig
    - Slack: [#web](https://artsy.slack.com/messages/web)
* Partner Engineering
    - Team lead: Dylan
    - Slack: [#pe](https://artsy.slack.com/messages/pe)

##### Engineering team standup
We have an engineering team-wide standup on *Mondays at 2 p.m.* where we give a high-level overview of what we worked on the previous week and what we hope to accomplish in the coming week.

##### Open Source Culture + Projects
At Artsy, we <3 open source and encourage you to become part of the community. Here is a [list of some open source technologies](http://artsy.github.io/open-source/) we are currently using.

Read dB’s blog post on [Becoming Open Source by Default](http://code.dblock.org/2015/02/09/becoming-open-source-by-default.html).

Read this [article by the mobile team](http://www.objc.io/issue-22/artsy.html) on the culture of open source at Artsy and their reasons behind open-sourcing our [mobile app](https://github.com/artsy/eigen).

Orta also wrote a blog post on the [mechanics behind open-sourcing Eigen](http://artsy.github.io/blog/2015/04/28/how-we-open-sourced-eigen/).

##### The Artsy Stack
This blog post by dB explains [our stack, circa 2015](http://artsy.github.io/blog/2015/03/23/artsy-technology-stack-2015/).

## Setting up your Dev Environment
Many of these are adopted from Joey’s gist: [How Joey Works](https://gist.github.com/joeyAghion/02dcf1d40829731525fb)

### Getting ready to Code

##### Text Editor
Most Artsy Engineers use [Sublime Text 2](http://www.sublimetext.com/2), but feel free to use whatever makes you most comfortable.

You can use the [Sublime Package Manager](https://packagecontrol.io/installation) to manage plugins in Sublime.

Once you have Package Manager installed, packages can be installed by following the [instructions here](https://packagecontrol.io/docs/usage). It all starts with `cmd+shift+p`.

If you do use Sublime, here are some plugins you might want to get you started:
* [git](https://packagecontrol.io/packages/Git)
* [git gutter](https://github.com/jisaacks/GitGutter)
* [Markdown preview](https://github.com/revolunet/sublimetext-markdown-preview)


### Making contributions

As all of our code is housed on Github, we make contributions through [pull requests](http://artsy.github.io/blog/2012/01/29/how-art-dot-sy-uses-github-to-build-art-dot-sy/).

If you are unfamiliar with Git, check out this [short tutorial](https://try.github.io) on basic git commands (such as `git status`, `git commit`, and `git push`).

If you'd like a more comprehensive review of Git and Github and how we use them, you can look at our Guide to [Git and Github](https://gist.github.com/gristleism/c2812efb2fc4daeee119).

##### Style guide

For a more indepth guide to our contribution workflow and our style preferences for Git and Pull Requests, you can view our [Style Guide](https://gist.github.com/gristleism/c2812efb2fc4daeee119).

The Github blog also has a nice article on [writing quality pull requests](https://github.com/blog/1943-how-to-write-the-perfect-pull-request).

### Deploying software

Once your pull request is merged, we use services like [Semaphore](https://semaphoreci.com/) and [Travis](https://magnum.travis-ci.com/) to run a full build of the app to make sure the code changes did not break existing features.

Most of our apps do not automatically deploy once the CI (continuous integration) step succeeds. Instead, you have to manually deploy the code to where it's hosted (usually either [Heroku](https://dashboard.heroku.com/) or [OpsWorks](https://console.aws.amazon.com/opsworks/home)). This process is app-specific, but generally done through the [Jenkins](http://joe.artsy.net:9000/) or Semaphore UI, or the command line.

We don't have a set deployment cycle for our web apps (developing for iOS is a different story...). At Artsy, we value small improvements through pull requests, and incremental deploys. You don't need permission to deploy-- you just have to announce when you plan to deploy something in the relevant slack channel in case someone is intentionally putting it off.

Our API app, Gravity, is hosted on OpsWorks. For more information on why we chose OpsWorks for this app, and *what it all means*, check out Joey's [Introduction to AWS OpsWorks](http://artsy.github.io/blog/2013/08/27/introduction-to-aws-opsworks/) blog post.

## If you get stuck

#### Slack
If you know what team could potentially help you, browse the channels in Slack to find the most relevant place to ask your question. If you aren't sure, [#dev](https://artsy.slack.com/messages/dev) is a good place to start.

#### Ask your neighbor
Everyone is really friendly-- don't hesitate to reach out to the people around you for even the most basic of questions.

---
## Team-Specific Onboarding

* [Platform](platform.md)
* Mobile
* PE
* Web

---
## Index of Docs

* Platform
    - [Platform Team Playbook](platform.md)
    - [Platform Team FAQ](platform_faq.md)
* Mobile
* PE
* Web
* General Engineering Practices
    - [Git and Github](https://gist.github.com/gristleism/c2812efb2fc4daeee119)
    - [Github Style Guide](https://gist.github.com/gristleism/967e4e7ad2da4f472aa6)
    - [Github Excercise](github_excercise.md)


### License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Artsy Potential</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://artsy.net" property="cc:attributionName" rel="cc:attributionURL">Artsy</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/artsy/potential" rel="dct:source">https://github.com/artsy/potential</a>.
