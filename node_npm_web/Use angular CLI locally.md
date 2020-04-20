
# Using Locally Installed Angular CLI

Having to install Angular CLI globally and contaminate the OS with another version of volatile software is annoying. Use NVM to manage node.js version and then use Angular CLI from a project-local instance would be more attractive. 

## Install NVM and Start Managing Node.js Versions

See [manage node.js using nvm](manage%20node.js%20using%20nvm.mdm.md).

* first ensure angular cli is not globally installed

# npm uninstall -g @angular/cli


* use npx to create a new project (dashboard-ui) in current folder
* - npx will download angular CLI into the "node_modules" folder in the new project folder

# npx -p @angular/cli@8.3.25 ng new dashboard-ui --style=scss

  
* run ng command using npx afterwards

# npx ng generate component my-component


