# superset_test_viz_plugin
Quick example plugin; serves as a reference for team members to get up and running quickly

## Development documentation

The following steps were necessary to develop the package.

### Install tools

The following command installs the node package manager (npm), which is needed for web frontend development:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
\. "$HOME/.nvm/nvm.sh"
nvm install 24

```

Next, we install the package named "yo" for all users. That package simplifies the generation of boilerplate code and will set up all the necessary directory structure for us.

```bash
npm i -g yo
```

Finally, we install the ``generator-superset`` package and symlink it.

```bash
cd <superset repo directory>/superset-frontend/packages/generator-superset
npm i
npm link
```

### Initialise codebase

Change to the directory in which we would like to develop our custom visualization plugin, then create the boilerplate code.

```bash
cd <my plugin repo dir>
yo @superset-ui/superset
```

Then you fill out all the required names etc.

Install the package:

```bash
npm install -f
```

### Setup development environment

Build the package: 

```bash
npm run build
```

Alternative, it is handy during development to run the following command in a terminal so that a rebuild is triggered automatically after each change:

```bash
npm run dev
```

Now we have to introduce our package to superset:

```bash
cd <superset repo directory>/superset-frontend/packages/generator-superset
```
