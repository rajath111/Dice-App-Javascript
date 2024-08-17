# P-DiceApp

This project has two parts. 

1. Creating Dice Appliction
I have used vanilla Javascript and HTML to build the dice app. The logic is fairly simple.

2. Deploy the application in Firebase
This was actually my first deployment. So, to keep it simple I chose firebase for hosting.


## Deploy to Firebase from Local machine
1. Install Firebase Cli
```
npm install -g firebase-tools
```

2. Login to firebase account
```
firebase login
firebase projects:list
```

3. Initialize the project
```
firebase init
```
This will provide different options like which Firebase services to use, path to application code, github action setup and much more.

4. Serve and test locally
```
firebase serve --only hosting
```

5. Deploying the application
```
firebase deploy -m "Deploying from local machine"
```

## Automatic Deployment with Github Actions
While doing firebase init, we get option to Set up automatic builds and deploys with GitHub. When you choose yes, then following things will be done automatically with our consent.

1. Provide permission to Upload Service account to GitHub repository's secret store. 
2. Select repository and branch name.
3. Firebase creates a service account, which has permission to deploy the code to the selected firebase project. And stores that in secrets of Github repository that was choosen.  ```<repo path>/settings/secrets```. We can manage these secrets afterwords also.
4. The association of firebase with our git hub account will be visible under Settings->Developer Settings->Integrations->Applications. We can revoke the permission to our Git repo from here.
5. 



