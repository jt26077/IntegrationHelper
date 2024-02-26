# IntegrationHelper
This repo is designed to help new developers setup integrations with Github and other best practices

Set up SSH keys

Windows:
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=windows

TL;DR
* `ssh-keygen -t ed25519 -C "your_email@example.com"`
* The default filename is fine, unless you're supporting multiple keys and need something more descriptive
* You can ignore the passphrase unless you're on a shared computer
* `start-ssh-agent` to restart the ssh-agent and pull in your new key
* `clip < ~/.ssh/id_ed25519.pub` to copy this to your clipboard. If you chose a different filename, replace that here

MacOS:
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=mac

TL;DR
* `ssh-keygen -t ed25519 -C "your_email@example.com"`
* The default filename is fine, unless you're supporting multiple keys and need something more descriptive
* You can ignore the passphrase unless you're on a shared computer
* `ssh-add --apple-use-keychain ~/.ssh/id_ed25519`
* `pbcopy < ~/.ssh/id_ed25519.pub` to copy this to your pasteboard. If you chose a different filename, replace that here

Add your new key to github:
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account

TL;DR
* https://github.com/settings/keys
* Click "New SSH Key"
* Paste the contents from the previous section into the dialog labeled "Key"
* Give the key a "Title" that makes sense fo you, ie: My Laptop, School Computer, etc...
* Click "Add SSH Key"