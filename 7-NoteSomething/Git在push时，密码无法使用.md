# How to Fix “Support for password authentication was removed” error in GitHub

5th April 2023   1 min read

![](https://usercontent.one/wp/collabnix.com/wp-content/uploads/2023/04/Screenshot-2023-04-05-at-12.51.50-PM.png)

GitHub is a popular platform for version control and collaboration, but in August 2021, GitHub removed support for password authentication for HTTPS URLs. This means that if you try to clone a repository using an HTTPS URL and authenticate with a password, you will receive the following error message: “Support for password authentication was removed on August 13, 2021.” Fortunately, you can fix this issue by switching to a personal access token (PAT) or an SSH URL.

I was trying to push my latest committed code to the remote GitHub repository, but faced the following error message:

```
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/collabnix/reponew'
```

To fix the “Support for password authentication was removed” error in GitHub, you need to switch to using a personal access token (PAT) instead of a password for authentication. Here are the steps to follow:

## Option 1: Use a Personal Access Token (PAT)

## Step 1. Create a personal access token (PAT) on GitHub

Login to your GitHub account. Go to Settings.

[![Image1](https://res.cloudinary.com/practicaldev/image/fetch/s--0NjybsOG--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/259q2s5n73ty3559vkip.png)](https://res.cloudinary.com/practicaldev/image/fetch/s--0NjybsOG--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/259q2s5n73ty3559vkip.png)

## Step 2. Generate a new token

Select “Developer settings,” and then “Personal access tokens.”

[![Image2](https://res.cloudinary.com/practicaldev/image/fetch/s--qVPmbhCT--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cbuv8n3aqkrhgvkkolmu.png)](https://res.cloudinary.com/practicaldev/image/fetch/s--qVPmbhCT--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cbuv8n3aqkrhgvkkolmu.png)

Next, you need to generate a new token by selecting the “Generate new token” button. Give your token a name and select the scopes you need. For cloning repositories, you need to select the “repo” scope.

[![Image3](https://res.cloudinary.com/practicaldev/image/fetch/s--Pr4WS8oi--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/nh5lovr31stkmbfo1tvl.png)](https://res.cloudinary.com/practicaldev/image/fetch/s--Pr4WS8oi--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/nh5lovr31stkmbfo1tvl.png)

## Step 3. Copy the token to your clipboard.

When prompted for your GitHub credentials while cloning a repository using an HTTPS URL, paste your PAT as your password.

## Option 2: Use an SSH URL

Alternatively, you can configure Git to use your PAT for all future interactions with GitHub by running the following command in your terminal:

```
git config --global credential.helper store
```

This command will save your credentials to a local file, so you don’t have to enter them every time you interact with GitHub. You can then enter your GitHub username as usual, and your PAT as your password.

Keep in mind that using an SSH URL to clone a repository is a more secure and recommended option, as it allows you to authenticate using your SSH key instead of a password or PAT.