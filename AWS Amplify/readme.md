# AWS Amplify Cheatsheet
## Set up AWS Environment

### Software to Install first:
- [Cocoapods](https://cocoapods.org)
- [NodeJS](https://nodejs.org/en/)
- [Homebrew](https://docs.brew.sh/Installation)
- [Npm](https://www.npmjs.com/get-npm)
- [Git](https://git-scm.com)


1. Open the terminal and type ```npm install -g @aws-amplify/cli```

2. Enter ``` amplify configure ```   [ Just sign in into your AWS account, then return back and press enter ] [Select region, enter username]

3. Copy and paste your access and **secret key** in the terminal. [set profile name to default ]
   
# AWS Initialization

1. Open terminal

2. Set terminal to project directory 

3. Type ```amplify init```

4. Enter name of project, environment, default editor, and set type of environment.

5. Set AWS profile to ```Yes and profile to default```



# AWS Commands

```amplify status``` : check status of environment 

``` amplify push ```:will build all your local backend resources and provision it in the cloud

```amplify add <category>```: will allow you to add features like user login or a backend API


```amplify console```: opens the AWS Amplify console in browser

```amplify publish```: builds all local backend and frontend resources (if you have hosting category added) and provision it in the cloud

```amplify remove <category>```to remove an individual resource

```amplify delete``` deletes entire Amplify project

- You can just type ``` amplify``` to get all the commands available!

# Terminal Tips
```cat <filename>```: to open file in terminal

```pwd```: to print current directory.

# AWS cognito Authentication

1. Open terminal, navigate to project directory and type ```amplify add auth```

2. Set authentication to ```Default Configuration```
Follow the steps in the terminal depending on what setting you want to use.

3. Use ```amplify status``` to check for any changes and use amplify push to send your configuration to the cloud
   
# Adding Cocoapods

1. Open terminal, navigate to project directory and type ```pod init```

2. Edit the podfile using Vim with ```vi <podfilename> ```or edit it directly using a text editor.

3. Add pod name under ```#Pods``` for ```<projectname>```

4. Save it and type ```pod install``` in the terminal.

5. Sit back, grab a cup of coffee☕️ and wait for it to install!

**Note:** After installing a podfile, open your project using the ```.xcworkspace```file to launch your projects

# AWS Appsync

1. Open terminal and type ```amplify add api```

2. Select api , name and type of authorization. ```[Graphql]```

3. Set annotated Graphql schema to ```No``` and schema creation to ```Yes``` [selected to ‘’to-do , edit -> yes’’]

4. Press enter and use ```amplify push``` to push to changes to cloud

5. Set generate newly Graphql API to ```Yes``` and follow the other defaults

6. Done!

# Graphql

```swift
type Todo @model {
  id: ID!
  name: String
  description: String
}
```
``` ! means an input is required for the field a.k.a not optional.```

# Edit Schema (IOS/Mac)


1. Open terminal and navigate to project directory
   
2. Goto ```‘’amplify”``` directory
   
3. Goto ```“backend”``` directory
   
4. Goto ```“api”``` directory
   
5. Goto ```“[project_name]”``` directory
   
6. Open ```“schema.graphql”``` file with vim ```[or type “vi schema.graphql”``` to open file]
   
7. Navigate back to project directory and type ```amplify push```
   
8.  Follow the self-explanatory steps in the terminal to update your graphql files.



```Credits```: 
- [chefThomas](https://gist.github.com/chefThomas)