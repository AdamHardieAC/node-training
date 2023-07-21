# Node Training Notes

### **Node**
  - Node.js is an open-sources runtime which allows developers to execute javascript code outside of the browser, allowing us to use the same language for both front and backend development, stream lining the development process. One other big advantage is being able to access and use the Node Package Manager (NPM), but we'll come to that later.
### **NPM**
  - NPM is Node Package Manager which is bundled with Node.js, used to install, manage, and share JavaScript packages. It allows us to handle project dependencies and access a wide range of reusable code, making it essential for Node.js development.
### **NPM vs Yarn**
  - NPM and Yarn are both JavaScript package managers, each with its strengths. Yarn is known for faster performance, deterministic dependency resolution, and a user-friendly CLI, while NPM boasts a vast and well-established package ecosystem. The choice between the two depends on specific project needs and priorities, with Yarn being preferred for speed and reliability, and NPM for its extensive package repository.
### **what package.json and package-lock.json/yarn.lock are for**
  - package.json - Config file for node proejcts, defines project details and listing required dependencies.
  - package-lock.json/yarn.lock - Lock files ensure consistent dependency versions which gives us the ability to create reproducible builds and prevents version conflicts.
### **NVM**
  - NVM (Node Version Manager) is a tool that lets developers manage multiple version of Node.js on the same machine, allowing us to easily switch between different Node.js environments for our projects.
### **.nvmrc**
  - .nvmrc - a configuration file which is used with NVM, allowing us to specify a particular version of node within the project. With this file being present in the project directory, we can easily allow developers to switch between node versions, project to project.
### **Installing dependencies, switching Node version & running tests**
#### Node commands
  - ```npm install <package_name>``` (or ```npm i <package_name>```) - This will fetch and install the ```<package_name>``` specified. 
    - Use the flag ```--save-dev``` to install a development specific dependency (most common with testing libraries).
  - ```npm install ``` (or ```npm i```) - This wil install the project dependencies which are listed within the `package.json` file.
  - ```npm run``` - this will list the available commands which can be used within the project.
  - ```npm <command_name>``` - this will run the specific ```<command_name>``` within the package.json file. The script which the command will run can be viewed within package.json too.
#### Switching Node version
changing node version with NVM is fairly simple, all we need to do is specifiy the node version of any given project within the .nvmrc file and running a couple of commands.
  - Open ```.nvmrc``` and change the version specified to the desired version. E.g. from 14.21.3 -> 18.17.0
  - ```nvm install``` - This will install the specified version of node within .nvmrc.
  - ```nvm use``` - This will switch node version to the version specified within .nvmrc.
    - If this version isn't installed already, you'll be prompted to install it first and then run this command again.
    - Once you've successfully switched node version, you'll want to run ```node -v``` & ```npm -v``` to verify that the correct versions is in use.

# Installing Node
- Download installer [here](https://nodejs.org/en/download) and go through the installation steps to install node locally.
# Installing NVM
- Download installer [here](https://github.com/coreybutler/nvm-windows/releases/download/1.1.11/nvm-setup.zip), extract the nvm-setup.exe file, run the file and go through the installation steps to install NVM locally. If there is a prompt to allow NVM to control the current version of Node on the system, click yes.
