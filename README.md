

## Purpose
* The motivation behind this repo is to understand how you can setup monorepos.
* It uses yarn workspaces and lerna.
* It helps you to co-locate all your projects for easier maintenance.
* You can also have private and public packages at one single place. 
* Private packages doesn't needs to be released to `npm` but still gives you the flexibility to share code across your projects just like any other `npm` package.

## Directory Structure
```
react-monorepo  
  |__api // api helpers as private package
  |__my-app // main application
  |__ui-kit // component library as private package
```

## Installation
Clone the repo and run
```
yarn
```
* This will install the packages listed in the root `package.json` as well as setup symlinks and install packages within all the projects listed in `workspaces: []` inside `package.json`.
* Once the installation is completed we run `lerna` which builds `api` and `ui-kit` as part of `postinstall` script.

## Start the application
Once the installation is done run following commands to start `my-app`
```
cd my-app
yarn start
```

## Like it?

:star: this repo
