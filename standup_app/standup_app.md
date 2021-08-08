# Building a Daily Standup Application in 30 Minutes

![Cover](https://i.imgur.com/cIavCTt.jpg)

The daily standup has become a norm in the schedule of most developers around the world. A standup is a daily team meeting, at a specific time for a specific duration, that asks team members to answer three major questions:

1. What did I work on yesterday?
1. What am I working on today?
1. What issues are blocking me?

The daily standup answers these questions but does not resolve them. When put to good use, daily standups increase team productivity and also enhance cohesion between all the parties involved.

## Tutorial Overview with Appsmith

In this tutorial, you’ll learn how to build a daily standup application using [Appsmith](https://www.appsmith.com/), an open-source framework for building internal tools, admin panels, dashboards, and workflows. You’ll be using Appsmith to forward a summary of daily standups to [Slack](https://slack.com/). Using a web framework like Appsmith is a much quicker way to add this feature to your workspace than building a completely new internal tool.

![page 1](https://i.imgur.com/6n1tlPd.png)

Appsmith comes out-of-the-box with prebuilt widgets like forms, charts, and maps that you can easily configure to your team’s needs. It also supports APIs and different types of databases. For more details about its capability, visit their official [GitHub page](https://github.com/appsmithorg/appsmith?utm_source=hashnode&utm_medium=blog&utm_content=standup_appsmith_tutorial&utm_campaign=weeklyblog&utm_term=standup_appsmith).

## Setting Up the Application and Data Model

First things first: head over to [Appsmith](https://www.appsmith.com/) to get a free account. After you sign up, it’s time to set up the user interface of your standup app.

* Click **Create New** on the dashboard to create a new app. You will be taken to an empty canvas as shown below where you can start creating your app. The explorer sidebar on the left is used to add widgets, create pages, and connect to APIs and data sources such as [Firestore](https://firebase.google.com/docs/firestore).

![page 2](https://i.imgur.com/PX8FIoD.png)

* To build all the features needed for this app, you’ll need to create two pages in Appsmith. Double-click **Page1** to rename it as First Page.

* On the Pages bar, click the **+** icon to add a page, then double-click to rename the new page as Second Page.

Now that you’ve created your two pages, it’s time to start adding widgets. Your app’s first page will contain:

* A personalized welcome message
* A paragraph showing yesterday's standup
* A text area where the user can enter what was done the previous day
* A text area to write out what they plan to do today
* An option field to show their blockers
* A table to show users who completed yesterday’s tasks
* Submit and reset buttons
Let’s create the custom welcome message next:

* Navigate to the **First Page** and click the **+** icon beside **Widgets** to add a new widget.
* Drag the text widget and drop it on the canvas.
* Type in a custom welcome message as shown below.

![page 3](https://i.imgur.com/kOERxvP.png)

Next, let’s display yesterday’s standup to-do on top so that you can see at a glance what you planned to do yesterday and then make plans based on that for today.

1. Add two text widgets side by side on your canvas.
1. Label the first Last Standup todo. The second widget will hold the value, or what was on the last standup to-do list. This will eventually be drawn from the database, but for now, you can pre-populate it with filler text.
1. Style the widget’s text as you prefer via the Settings gear at the top right of each widget.

![page 4](https://i.imgur.com/nmiOVE9.png)
