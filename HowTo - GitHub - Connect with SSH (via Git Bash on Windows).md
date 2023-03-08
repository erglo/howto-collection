# GitHub - Connect with SSH (_using Git Bash on Windows_)

REF.: [GitHub Docs - Checking for existing SSH keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys)  
REF.: [GitHub Docs - Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)  
REF.: [GitHub Docs - Adding a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)  
REF.: [Git - git-config Documentation - `user.signingKey`](https://git-scm.com/docs/git-config#Documentation/git-config.txt-usersigningKey)  
REF.: [GitHub Docs - Switching remote URLs from HTTPS to SSH](https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories#switching-remote-urls-from-https-to-ssh)  

**Note:**  
If you haven't used your SSH key for a year, GitHub will automatically delete your inactive SSH key as a security precaution.  
This is a step-by-step TL;DR style walkthrough.  

----

## Checking for existing SSH keys

```bash
$ ls -al ~/.ssh
# Lists the files in your .ssh directory, if they exist
```

If you receive an error that `~/.ssh` doesn't exist, you do _not_ have an existing SSH key pair in the default location. Either generate a new SSH key or upload an existing key.  
By default, the filenames of supported public keys for GitHub are one of the following.

- `id_rsa.pub`  
- `id_ecdsa.pub`  
- `id_ed25519.pub`  

----

## Ensure the ssh-agent is running

```bash
# Start the ssh-agent in the background
$ eval "$(ssh-agent -s)"
> Agent pid 59566
```

----

## Generating a new SSH key

```bash
$ ssh-keygen -t ed25519 -C "your_email@example.com"
# You will be prompted for the file location and the passphrase
# (See notes below)
```

- When you're prompted to "Enter a file in which to save the key", you can press `Enter` to accept the default file location. Please note that if you created SSH keys previously, ssh-keygen may ask you to rewrite another key, in which case we recommend creating a custom-named SSH key. To do so, type the default file location and replace id_ssh_keyname with your custom key name.  
- Type a secure passphrase (twice).

## Adding your SSH key to the ssh-agent

```bash
$ ssh-add ~/.ssh/id_ed25519
# You will be prompted for your passphrase
```

----

## Adding the SSH key to your account on GitHub

```bash
$ clip < ~/.ssh/id_ed25519.pub
# Copies the contents of the id_ed25519.pub file to your clipboard
# Note: Do NOT forget '<'!
# Alternatively open the file and copy its content.
```

- Log-in to GitHub, go to (account) Settings > SSH and GPG keys, click "New SSH key"
- Enter a descriptive name to "Title", eg. the name of your local machine and paste the previous copied file content to "Key".

----

## Switching remote URLs from HTTPS to SSH

### Listing existing remotes

```bash
$ git remote -v
> origin  https://github.com/USERNAME/REPOSITORY.git (fetch)
> origin  https://github.com/USERNAME/REPOSITORY.git (push)
```

### Changing your remote's URL

```bash
$ git remote set-url origin git@github.com:USERNAME/REPOSITORY.git
# or copy the URL from your repository's GitHub page
# Verify change by listing existing remote (see one step above)
```
