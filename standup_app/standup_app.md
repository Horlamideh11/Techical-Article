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

As mentioned earlier, the goal of a standup is to provide information about the previous day’s tasks, tasks that need to be done today, and anything standing in the way of accomplishing those tasks. Obviously, you’ll need a form to input all that information.

To create a form:

1. Drag the form widget from the sidebar onto the canvas.
1. Label the inputs or dropdowns appropriately (eg, User, Yesterday’s todos, Yesterday completed, and so on). Note that the form widget comes out-of-the-box with **Reset** and **Submit** buttons.

![page 5](https://i.imgur.com/0zGtBRJ.png)

1. Rename the form by double-clicking on the default name and editing it. Naming this particular form seemed unnecessary, so that the title widget in the form was deleted.
1. To delete a widget, hover over it, then right-click the widget name at the top right corner. In the dropdown menu, you’ll see a Delete option. Click to delete the widget.

To finalize your first page’s UI, let’s add a table to display the users who’ve submitted their standup for the day:

1. Drag the table widget onto the canvas. Note that the Table Data option in this widget already contains an array of objects. Later, you’ll change this to a query response from your database.

![page 6](https://i.imgur.com/WVzdmXT.png)

1. Navigate to your Second Page, where you’ll add your table.
1. Drag the table widget onto the canvas.
1. Open the table options and add a new column called Actions.
1. Click the Settings gear above the Actions column and set the following properties:
    1. Column Type: Button
    1. Label: Edit
    1. onClick: OpenModal
    1. Modal Name: New Modal

![page 7](https://i.imgur.com/eTkRJ4h.png)

1. In the Actions column you just created, click the button that now reads Edit. A new modal will popup, which you’ll use to edit the table’s data.
1. Change the title text widget to Edit Table.
1. Drag a text widget into the modal and set the following properties:
    1. Text value: Username
    1. Text align: Left
    1. Text style: Label

1. Add a dropdown widget beside the label you just created. In the Settings for that widget, set Selection type to Single Select. This dropdown, which ought to display all users of your app, will read data from your database after connecting the database to Appsmith later in this tutorial.
1. To add a field for blockers, drop in a text widget, name it Blocker, and add a dropdown widget as you’ve done previously.
1. Add one field each for today’s to-do and yesterday’s to-do. These will take a text widget and an input widget each.
1. Finally, add a field to confirm if yesterday’s to-do is complete. Drag over a text widget and a dropdown widget with the values Yes or No.

![page 8](https://i.imgur.com/PdjNbmq.png)
