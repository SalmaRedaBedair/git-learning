# GIT
- github simplify using hit
- gitlab and bitbucket are also used with git behind github
- we upload our project to centerolized server, git is not related only with github
- with git we can revert some changes... revert mean cancel
- 
![](./images/git1.png)
## git clone
- we use it to download github project to pc
## Reset
```git
git reset head file_name.extension
```
- that command remove file that we add to staging area using git add
## status
```
git status
```
- that command is used to know what are the files in stage area, that need to commit
## git branch
- with it i can know all branches in my repo
## git remote -v
- tell me what are the remote repos i work in
## git push
- git push remoteName branchName
    - ex: git push origin master
## configaration 
- you can change any thing you want in git like user name, email or colors
## how to generate public key in github
Generating a public key for GitHub involves creating an SSH key pair, consisting of a public key and a private key. Here's a step-by-step guide on how to do it:

1. **Open a Terminal**: Start by opening a terminal window on your computer.

2. **Generate SSH Key Pair**: Use the `ssh-keygen` command to generate an SSH key pair. The `-t` flag specifies the key type (RSA in this case), and the `-b` flag specifies the key's bit length (usually 4096 bits is recommended for security). Here's the command:

   ```shell
   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```

   Replace `"your_email@example.com"` with the email associated with your GitHub account.

   - `ssh-keygen`: This command generates the key pair.
   - `-t rsa`: Specifies the key type as RSA.
   - `-b 4096`: Sets the key length to 4096 bits for increased security.
   - `-C "your_email@example.com"`: Adds a comment to identify the key (usually your email).

3. **Save the Key**: After running the command, you'll be prompted to choose where to save the key. Press Enter to accept the default location, typically `~/.ssh/id_rsa` for the private key and `~/.ssh/id_rsa.pub` for the public key.

4. **Set a Passphrase (Optional)**: You can choose to set a passphrase for additional security. This passphrase is required to use the private key.

5. **View the Public Key**: To view the contents of the public key, you can use the `cat` command:

   ```shell
   cat ~/.ssh/id_rsa.pub
   ```

   This command will display the public key in your terminal.

6. **Copy the Public Key**: Select and copy the entire content of the public key that is displayed in your terminal.

7. **Add the Public Key to GitHub**:
   - Log in to your GitHub account.
   - Go to your account settings by clicking on your profile picture in the top right corner, then select "Settings."
   - In the left sidebar, click on "SSH and GPG keys."
   - Click on the "New SSH key" button.
   - Give your key a descriptive title.
   - Paste the copied public key into the "Key" field.
   - Click the "Add SSH key" button to save it.
