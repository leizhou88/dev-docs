
* first ensure angular cli is not globally installed

# npm uninstall -g @angular/cli


* use npx to create a new project (dashboard-ui) in current folder
* - npx will download angular CLI into the "node_modules" folder in the new project folder

# npx -p @angular/cli@8.3.25 ng new dashboard-ui --style=scss

  
* run ng command using npx afterwards

# npx ng generate component my-component


