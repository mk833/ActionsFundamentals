# 🔨 Hands-on: My first IssueOps

In this hands-on lab you will create your first GitHub IssueOps template and learn how you can use Issues to drive workflows. If you like more background information, please refer to the [GitHub IssueOps](https://issue-ops.github.io/docs/) pages on GitHub Docs. Good luck! 👍

This lab has a pre-requisite of completing the first hands on lab [01-My-first-workflow](/lab/01-My-first-workflow.md)

This hands on lab consists of the following steps:
- [Creating an issue form]()
- [Adding a new issue form for use]()
- 


## Creating an issue form

1. create issue template folder and add a file, bug report
2. add content to the file. Have the form set the labels "bug" and "triage". In the body of the form we want: 
- a contact input for an email address 
- a text area that can be used for details
- a required dropdown to choose one or more browsers 

<details>
    <summary>Solution</summary>

```YAML
name: Bug Report
description: File a bug report.
title: "[Bug]: "
labels: ["bug", "triage"]
body:
    - type: input
      id: contact
      attributes:
        label: Contact Details
        description: How can we get in touch with you if we need more info?
        placeholder: ex. email@example.com
    - type: textarea
      id: what-happened
      attributes:
        label: What happened?
        description: Also tell us, what did you expect to happen?
        placeholder: Tell us what you see!
        value: "A bug happened"
    - type: dropdown
      id: browsers
      attributes:
        label: What browsers are you seeing the problem on?
        multiple: true
        options:
          - Firefox
          - Chrome
          - Safari
          - Microsoft Edge
      validations:
        required: true

```
</details>

3. Save and commit your changes to the repo. If you are using a branch, merge your changes into main.

## Adding a new issue form for use

1. To prepare for using the new form, we need to add a new label. Go to [labels](/../../labels) and add 'triage'.
2. Go to **Issues** | [New Bug report](/../../issues/new?template=bug-report.yml)
3. Fill in the bug report form and create it. Validate that you have both labels on your issue.

## Adding a workflow trigger

1. Open the workflow that you created for the first HOL lab, `github-actions-demo.yml`. Make a copy of this file and name it `github-issues-demo.yml`
2. Remove any triggers, so that only `workflow-dispatch` remains
3. Add triggers to the workflow:
- when an issue is opened
- when an issue is edited
4. Save and commit your updates to main
5. Create a new issue and navigate to the Actions tab to view your newly created workflow run. 