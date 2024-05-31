# 17 CS | Regex Tutorial

## The Challenge: 

Your assignment this week is to create a tutorial that explains how a specific regular expression, or regex, functions by breaking down each part of the expression and describing what it does. You'll use the template provided in the starter code to create your walkthrough.

## Project Conduction:

As a web development student, I want a tutorial explaining a specific regex, then I can have a better understanding about the search pattern that regex defines.


## Acceptance Criteria:

- Given a regex tutorial, when the user opens the tutorial
they see the following:
    - descriptive title
    - introductory paragraph explaining the purpose of the tutorial
    - a summary describing the regex featured in the tutorial
    - a table of contents linking to different sections that break down each component of the regex and explain what it does
    - a section about the author with a link to the author’s GitHub profile

- When the user clicks on the links in the table of contents, they are taken to the corresponding sections of the tutorial.

- When the user reads through each section of the tutorial, they find a detailed explanation of what a specific component of the regex does.

- When the user reaches the end of the tutorial, they find a section about the author and a link to the author’s GitHub profile.


#### Short List

* Include all of the sections that correspond to the different components of the regex you chose.

* Each section that describes a component must include more than just one sentence explaining what it does, be thourogh.

* Each section that describes a component must include a code snippet of that particular component. Use backticks to display your code snippets in Markdown.

* Each section that describes a component must include at least one example that meets the requirements of that component.


## The Deployment:

The Gist: [Click Here.](https://github.com/NovaLanceBrittany/HW-18-NoSQL-Network-API)







## What Is a Regex?

A **regex**, which is short for **regular expression**, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input. 

For example, the following regular expression can be used to verify that user input is a valid email address:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Each component of this regex has a unique responsibility to make sure that a user enters an email address that begins with an unspecified number of characters preceding the `@` symbol, followed by a domain.

Before you get started, watch this [introduction to regular expressions video](https://youtu.be/7DG3kCDx53c) and read [Regex Tutorial: Matching a Username](https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial) to learn how to identify the different components that make up a regex. If you need any additional help, there are many resources on the web. Feel free to do your own research to find one that can help you complete this assignment.

Once you have a better understanding of what these different parts of a regular expression do, you’ll need to explain what they do for a specific regex.

You can choose one of the following regular expressions or you can choose one that you found on your own (with the exception of the one that is covered in the [Regex Tutorial: Matching a Username](https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial):

* Matching a Hex Value: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`


> **Important**: Make sure to create a **public** gist and add the `.md` file extension to the file name so that your Markdown renders correctly.

The starter code is a template with a title, introductory paragraph, summary, and table of contents. The table of contents should link to sections of the tutorial that describe the functionality of each component in the regex. Be sure to rename the template to a unique name that describes your tutorial.

> **Note**: The regular expression that you choose might not include all of the components outlined in the starter code. After you’ve finished your walkthrough, you can remove any sections that you didn’t use.

Each section that describes a component should include more than just one sentence explaining what it does. It should also include a code snippet of that particular component and some examples that meet the requirements of that component.

> **Important**: Make revisions to your gist in the GitHub gist UI. This will create a revision history that graders can use to verify that the tutorial content is yours.

## Grading Requirements


* Your GitHub gist that contains the tutorial Markdown. Your gist must include the `.md` file extension so that your Markdown renders correctly.



