My Electron app is a constellation front end cloned from https://github.com/jschiarizzi/eyestreet



## Debugging
On OSX, my first npm build failed.

Using the <help me troubleshoot> tab, _nvm install 6.11.2_ failed because it didn't think nvm was a command.

### Steps to fix
- Run _$ ~/.nvm/nvm.sh_ to see if that is a file. It was not
- Run _$curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash_
- Run _$source ~/.nvm/nvm.sh_
- Now the nvm commands from the help tab will work, and the project can be built.
