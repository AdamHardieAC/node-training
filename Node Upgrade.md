# Steps to upgrade node version of a project.

- Update the .nvmrc file within the project root directory to be the version of node which you'd like to upgrade to. For example, updating from 14.21.3 to 18.17.0.
- Now we need to check if there is an engines property within package.json and update the engine values to correspond to our .nvmrc version.
- Next, we need to run ```nvm install```, installing the version of node which we specified in our .nvmrc file. After this installation, we need to run ```nvm use```, switching our current system version of node, to the version which we've just installed.
- If there is one, delete the node_modules/ directory as we will need to re-download our node_modules to be current with the newly installed version of node.
- To do this, we need to run ```npm i```, which will install the necessary dependencies for the project within the node_modules/ directory.
- After installing our dependencies, we will need to run through all of the scripts which are specified within our package.json file, in order to verify that the project still works as intended after upgrading node version.
  - To view all of the scripts which are available to run, execute the following command ```npm run```, this will list each command and what it does.
  - run each command individually from this list to verfiy that things are working as intended.