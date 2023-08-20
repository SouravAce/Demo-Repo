# Demo

Hey, I am using Git now!

INSTALLING GIT ON MAC 

When tried to check if Git was present in MAC 
--> git --version 

Got below error 
--> xcrun: error: invalid active developer path (/Library/Developer/CommandLineTools), missing xcrun at: /Library/Developer/CommandLineTools/usr/bin/xcrun

Then referred to a youtube video and executed the below command  
--> xcode-select --install
xcode-select: note: install requested for command line developer tools

Now git is installed 
--> git --version
git version 2.39.2 (Apple Git-143)

HOW TO GENERATE SSH KEY

Generating a new SSH key and adding it to the ssh-agent

1. Open Terminal.
2. Paste the text below, substituting it in your GitHub email address.
   -->  ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

   Generating public/private ed25519 key pair.
   Enter file in which to save the key (/Users/sourav/.ssh/id_ed25519): 
   Enter passphrase (empty for no passphrase): 
   Enter same passphrase again: 
   Your identification has been saved in /Users/sourav/.ssh/id_ed25519
   Your public key has been saved in /Users/sourav/.ssh/id_ed25519.pub
   The key fingerprint is:

Adding your SSH key to the ssh-agent

1. Paste the text below on the Terminal
   -->  eval "$(ssh-agent -s)"
   Agent pid 59566

   --> nano ~/.ssh/config
   
3. After opening SSH paste the below text.
   -->Host github.com
      AddKeysToAgent yes
      UseKeychain yes
      IdentityFile ~/.ssh/id_ed25519
   
   --> open ~/.ssh/config
   --> ssh-add --apple-use-keychain ~/.ssh/id_ed25519
   
5. Now copy the SSH key using the below text and adding it to the ssh-agent  
   --> pbcopy < ~/.ssh/id_ed25519.pub 
   
   
