# Mobile Practice Playbook

## Team Information

### Culture

We collectively created an article for the magazine [objc.io on Artsy Mobiles's culture](http://www.objc.io/issue-22/artsy.html).

### Team Goals

* Create delightful, focused, mobile native experiences.
* Aggressively Open by Default.

### Who is on the Mobile Practice?

Current members of the Mobile Practice can be found on the [Artsy/Mobile](https://github.com/artsy/mobile/) GitHub repo.

### Logistics

* Bi-weekly stand-up on Tuesday / Thursday 11:00 (NYC time)
    * What are you working on or need help with?
    * Explain any new features or requests.

* Work is done through GitHub issues within sprint cycles.
    * Sprint Cycles timing varies between projects.
    * Milestones, and features are discussed and setup at a pre-sprint meeting.
    * Issues are created and added to the sprint milestone.

* Team-wide issues and TODOs can be found in [Artsy/Mobile](https://github.com/artsy/mobile/).
* The Mobile team specific [calendar](https://www.google.com/calendar/embed?src=artsymail.com_bke4sctkn8o072rjgtcsrrun3s%40group.calendar.google.com&ctz=America/New_York) is used for Out Of Office / Events.
* Chat in [#mobile](https://artsy.slack.com/messages/mobile/)
* Each app has its own focused channel in Slack [#eigen](https://artsy.slack.com/messages/eigen/), [#folio](https://artsy.slack.com/messages/folio) and [#eidolon](https://artsy.slack.com/messages/eidolon/).
* GitHub notifications, etc. in [#mobile-notifications](https://artsy.slack.com/messages/mobile-notifications/).
* Certificates and keys for signing apps for development/distribution are in the Engineering 1Password vault. The certs/keys are stored as a developer identity that can be imported into Xcode; the entry is named "Apple iOS Mobile Developer Identity". Make sure to install from there instead of letting Xcode revoke the existing keys.

  For more information related to choosing the right certificate and profile for development builds (that include Push Notification support), see [this document](https://github.com/artsy/eigen/blob/master/docs/push_notifications.md). In case you need to manually install the right certificate, it is called “Eigen Developer Identity” in the Engineering 1Password vault.

### Our Apps

* [Eigen](https://github.com/artsy/eigen): The Artsy iOS App.
* [Energy](https://github.com/artsy/energy): Artsy Partner's Portfolio App.
* [Eidolon](https://github.com/artsy/eidolon): Kiosk App for Auctions.

* See the [engineering projects map](https://trello.com/b/VLlTIM7l/artsy-engineering-projects-map) for a comprehensive list of Mobile Practice libraries.

### Our Key Technologies

#### Objective-C

Swift is nice, but not ready for mixing with our larger Objective-C code bases.

#### CocoaPods + Bundler

We rely on dependency managers, and plugins for them. If this is new to you, we recommend reading the [Podfiles](https://guides.cocoapods.org/) and [Gemfiles](https://guides.cocoapods.org/using/a-gemfile.html) guides on CocoaPods.

#### Testing

We test our apps to ensure that our behavior is what we expect. We use a collection of [FBSnapshot](http://www.objc.io/issue-15/snapshot-testing.html) Tests and Unit Tests via [Specta/Expecta](https://github.com/specta/specta) or [Quick/Nimble](https://github.com/Quick/Quick/).

#### Eigen

* **Useful:** [ORStackView](https://github.com/orta/ORStackView/), [ARAnalytics](https://github.com/orta/ARAnalytics) + [RAC DSL](https://github.com/artsy/eigen/blob/6bcacede194ca5b948e916746d313e7c96ec085e/Artsy/Classes/ARAppDelegate%2BAnalytics.m) and [ReactiveCocoa](http://reactivecocoa.io).
* **Essentials:** Auto Layout, [JLRoutes](https://github.com/joeldev/JLRoutes)

#### Energy

* **Useful:** [ORStackView](https://github.com/orta/ORStackView/), [ARAnalytics](https://github.com/orta/ARAnalytics).
* **Essentials:** Core Data, [DRBOperationTree](https://cocoapods.org/pods/DRBOperationTree)

#### Eidolon

* **Essentials:** Swift, [ReactiveCocoa](http://reactivecocoa.io), [Moya](https://github.com/ashfurrow/moya/), Storyboards
