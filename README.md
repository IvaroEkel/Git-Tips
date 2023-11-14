# Git-Tips
Sources of tips on Git commands, authentication using PAT, etc.

-Securely storing PAT locally in Ubuntu: https://www.pragmaticlinux.com/2023/05/create-and-store-your-github-personal-access-token/
  usint GNOME-keyring, works for Debian/Ubuntu/Raspberry PI

- sudo apt install make gcc libsecret-1-0 libsecret-1-dev
- cd /usr/share/doc/git/contrib/credential/libsecret
- sudo make
- git config --global credential.helper /usr/share/doc/git/contrib/credential/libsecret/git-credential-libsecret

*The next time your perform a GIT operation, requiring credentials, the credential helper stores the username and personal access token in your GNOME keyring. For subsequent GIT operations, your credentials are automatically taken from the stored values in your GNOME keyring. To change or delete the credentials stored in the GNOME keyring, you can use a GUI tool such as Seahorse
