# Workspace Test 

Requires NPM 7

```bash
npm i npm@7
```

Hosts two workspaces:

* UI - [tsdx](https://tsdx.io/) repository for creating a TS library.
* Frontend - created using [create-react-app](https://create-react-app.dev/)

Frontend repository has a depedency on UI.

```bash
+-- package.json
+-- node_modules
  ├── ui #symlinked
+-- ui
  ├── package.json
+-- frontend
  ├── package.json  # has dependency for ui
```

Workspaces ensures that the ui dependency is upto date and symlink is used. So publishing isn't necessary to use it.

# Usage 

In the root of workspace:

```bash
npm i # Installs depedency for both UI and frontend
npm start # Starts up frontend
npm run watch-ui # watches UI for changes and recompiles 
```

