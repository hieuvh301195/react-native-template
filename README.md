# hieuvh3011/react-native-template

## Introduction
Hi guys. This is a template I made for myself, since I have so much of pet projects and I'm so tired to re create project every times I had a new idea. You are welcome to use it. 

This template is inspire by [moove-it/react-native-template](https://github.com/moove-it/react-native-template). Therefore, you could see some similarity between my template and them. I create my own template because of their coding styles is not match to mine.

## Dependencies
- [Axios](https://github.com/axios/axios): for networking.
- Full dependencies of [React-Navigation](https://reactnavigation.org/docs/hello-react-navigation): use to manage navigation of app.
- [Redux-Toolkit](https://redux-toolkit.js.org/): a new, recommended version of [Redux](https://redux.js.org/introduction/getting-started), make redux is easier to use.
- [React-Redux](https://github.com/reduxjs/react-redux): package to use Redux with React (and/or React Native).
- [React-Native-Rename](https://github.com/junedomingo/react-native-rename): use to rename your project if you clone this template. 
- [Redux-Thunk](https://github.com/reduxjs/redux-thunk): to dispatch asynchronous actions.
- [Jest](https://facebook.github.io/jest/): for testing.

## Usage
### Option 1: create project with template
Step 1: init project
```bash
$ npx react-native init YourProjectName --template react-native-template-ts
```
Step 2: install all dependencies:
```bash
$ yarn install
```
or
```bash
$ npm install
```
### Option 2: create project by clone
Step 1: clone project from git
```bash
$ git clone https://github.com/hieuvh301195/react-native-ts-template.git
```
or you can clone by SSH:
```bash
$ git clone git@github.com:hieuvh301195/react-native-ts-template.git
```
Step 2: install all dependencies:
```bash
$ yarn install
```
or
```bash
$ npm install
```
Step 3: rename project
```bash
$ npx react-native-rename YourProjectName
```

## Folder structure
As I mentioned above, this template is inspire by js template *react-native-template*. Hence, it follows project structure similar to *react-native-template* (and similar to almost all of react native project that I have ever seen):
- `src`: This folder is the main container of all the code inside of your application.
  - `actions`: This folder contains all actions that can be dispatched to redux.
  - `assets`: Asset folder to store all images, vectors, etc.
  - `components`: Components folder contains all your application components.
    - `commons`: Folder to store any common component that you use through your app (such as a generic button, text fields, etc).
    - `MyComponent`: Each component should be stored inside it's own folder. Some of developers would like to split styles.js to a file. But for me, I am much more prefer with styling inside of component. Structure inside of this folder is completely depend on you. For me, I use this:
      - `MyComponent.tsx`: is a file code for main UI on screen.
      - `SomeSmallComponent.tsx`: is a file code for some small component in `MyComponent` screen. I split it so it make `MyComponent.tsx` shorter and easy to read.
      - `MyComponentViewModel.tsx`: This file control all of local states, navigation, logics, etc in `MyComponent`. It use **React Hook** to split UI and logic. You can read it at [here](https://medium.com/@sairysss/react-separating-responsibilities-using-hooks-b9c90dbb3ab9). If you are using Class instead of Hook, feel free to add [Recompose](https://github.com/acdlite/recompose) for similar function.
  - `helpers`: Folder to store any kind of helper that you have, such as Themes, Colors, Dimensions, etc.
  - `reducers`: This folder should have all your reducers, and expose the combined result using its `index.js`
  - `store`: use to create store for all of global states in your application.
  - `api`: Folder to store all your network activities.
  - `business_logic`: Folder to store all your business logic (if it has).
- `App.js`: Main component that starts your whole app.
- `index.js`: Entry point of your application as per React-Native standards.