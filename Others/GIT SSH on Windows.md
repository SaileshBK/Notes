## Reference

[[https://docs.github.com/en/authentication/connecting-to-github-with-ssh]]

## Generating a new SSH key

1. Make sure we have /c/Users/YOU/.ssh folder
2. Open Git Bash

```
ssh-keygen -t ed25519 -C "your_email@example.com"
```

when it prompts you to "> Enter file in which to save the key (/c/Users/YOU/.ssh/id_ALGORITHM):[Press enter]", we need to provide :

```
/c/Users/YOU/.ssh/test_personal_key
```

This will create a new SSH keys, in .ssh folder.

## Adding your SSH key to the ssh-agent

Now open PowerShell as admin and run the following:

```
Get-Service -Name ssh-agent | Set-Service -StartupType Manual

Start-Service ssh-agent
```

This will start the ssh-agent in the background.

Now open Git Bash and run the following commands:

```
ssh-add ~/.ssh/test_personal_key
```

This will add your SSH key to the ssh-agent.

## Adding a new SSH key to Github account

Navigate to the /c/Users/YOU/.ssh/test_personal_key.pub and cat that out.

```
cat /c/Users/YOU/.ssh/test_personal_key.pub
```

Copy the output and paste it in the SSH and GPG keys section of your Github account.

## Configure SSH Config file

In Git Bash, run the following command:

```
touch ~/.ssh/config
```

Tis will create a new file called config in the .ssh folder. Now open the config file and add the following:

```
Host my_personal_key
  HostName github.com
  User git
  IdentityFile ~/.ssh/test_personal_key
  IdentitiesOnly yes
```

## Cloning a repository using SSH

```
git clone git@my_personal_key:username/repository.git
```

## Debugging

1. Test the SSH Connection

```
ssh -T git@github.com
```

2. Ensure the SSH agent is running

```
eval $(ssh-agent -s)
```
