# GitHub OAuth Authentication Setup

This guide will walk you through the steps to set up GitHub OAuth authentication for your web application. By the end of this setup, your application will be able to authenticate users using their GitHub accounts.

## Prerequisites
- A GitHub account. If you don't have one, sign up [here](https://github.com/join).
- A web application where you will integrate GitHub OAuth authentication.

## Steps to Set Up GitHub OAuth Application

### 1. Register an OAuth Application on GitHub

1. **Sign in to your GitHub account** and navigate to your **Settings** page by clicking on your GitHub icon at the top-right corner.
2. In the **Settings** page, select **Developer settings** in the sidebar.
3. Under **Developer settings**, choose **OAuth Apps** from the sidebar.
4. Click on the **Register a new application** button.

### 2. Fill Out the Application Registration Form

Fill out the form with the following information:

- **Application Name**: OAuth Project (or any name for your project)
- **Homepage URL**: `http://localhost:3000` (for local development)
- **Authorization Callback URL**: `http://localhost:3000/auth/github/callback`

After filling in the details, click **Register application**.

### 3. Generate Client ID and Client Secret

Once registered, you will be provided with a **Client ID**. 

- Click on **Generate a new client secret** to generate the **Client Secret**.
- Copy both your **Client ID** and **Client Secret** and paste them into a text file in a secure location, as the Client Secret will only be shown once.

### 4. Set Up the Environment Variables

Next, we will configure the environment variables in your application to store the GitHub OAuth credentials securely.

1. Inside the `starting-code/` directory of your project, locate the `.env` file. If you don’t see the `.env` file, you might need to enable the option to view hidden files in your file explorer.

2. Open the `.env` file and add the following values:

