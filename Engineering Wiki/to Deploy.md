# How to Deploy

Use this template to describe the steps engineers should follow to deploy. 

# 1. Ping in Slack #deploys channel

Let everyone know you're about to start a deploy. 

# 2. SSH into the deployment server

Create a code block by typing `/code` and pressing `enter`.

```bash
ssh deployments.acmecorp.com
```

- You can create `inline code snippets` with the shortcut `cmd/ctrl + e`.

# 3. Run the following commands

```bash
acme deploy --prod
```