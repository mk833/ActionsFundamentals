# 🔨 Hands-on: My first IssueOps issue parse

In this hands-on lab you will create your first GitHub IssueOps parse workflow. If you like more background information, please refer to the [GitHub IssueOps](https://issue-ops.github.io/docs/) pages on GitHub Docs. Good luck! 👍


This hands on lab consists of the following steps:
- [Creating an issue form]()
- [Adding a new issue form for use]()
- [Adding a new issue parse workflow]()
- [Adding a write-back (optional)]()


## Creating an issue form

1. create issue template folder and add a file, bug report
2. add content to the file. Have the form set the labels "bug" and "triage". In the body of the form we want: 
- a contact input for an email address 
- a text area that can be used for details
- a required dropdown to choose one or more browsers

<details>
    <summary>Solution</summary>
TODO
```YAML


```
</details>

3. Save and commit your changes to the repo. If you are using a branch, merge your changes into main
TODO 4. To prepare for using the new form, we need to add a new label. Go to [labels](/../../labels) and add 'xxxxx'.

## Adding a new issue form for use

1. 
2. Go to **Issues** | [New Bug report](/../../issues/new?template=bug-report.yml)
TODO 3. Fill in the XXX form and create it. Validate that you have all of your labels are on your issue. FIX

## Adding a new issue parse workflow

1. Create a new workflow file and name it `github-parse-demo.yml`
2. Add a 
3. Add triggers to the workflow:
- when an issue is opened
- when an issue is edited
4. Save and commit your updates to main
5. Create a new issue and navigate to the Actions tab to view your newly created workflow run. 

## Adding a write-back (optional)