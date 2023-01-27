# starter-vue-basic

__A basic Vue 3 app starter, with a zero-build developer-experience.__

∅&nbsp; __Version:__ 0.0.1  
∅&nbsp; __Repo:__ <https://github.com/0bdx/starter-vue-basic>  
∅&nbsp; __Homepage:__ <https://0bdx.com/starter-vue-basic>

@TODO add an overview

---

## How to create a repo like this, from scratch

### __1. Create the repo__

1. At GitHub, click the ‘+’ icon, and ‘New repository’
2. Name it, describe it, tick ‘Add a README file’, choose MIT license
3. Click ‘Create repository’
4. Click the ‘Code’ button, ‘Local’ tab, ‘SSH’, and the copy icon
5. In your Terminal, `cd` to wherever you work
6. `git clone ` and paste something like ‘git@github.com:kim/my-app.git’
7. `cd` into the new directory, eg `cd my-app`

### __2. Create the .gitignore file__

```
.DS_Store
node_modules
node_modules.zip
```

### __3. Create the package.json file__

1. Create a default __package.json__ file:  
   `npm init --yes`
2. Change the version to 0.0.1:  
   `sed -ix 's/: "1.0.0",/: "0.0.1",/' *.json`
3. Insert your name, email and domain:  
   `sed -ix 's/"author": "/"author": "0bdx <hi@0bdx.com> (0bdx.com)/' *.json`
4. Change the license to MIT:  
   `sed -ix 's/: "ISC",/: "MIT",/' *.json`
5. Remove the ‘main’ property because this is an app not a library,  
   and also tell Node to use `import` not `require()` (avoids needing .mjs):  
   `sed -ix 's/"main": "index.js"/"type": "module"/' *.json`
6. Delete the temporary __package.jsonx__ file:  
   `rm package.jsonx`

Or as a single command you can copy-and-paste:
```sh
npm init --yes
sed -ix 's/: "1.0.0",/: "0.0.1",/' *.json
sed -ix 's/"author": "/"author": "0bdx <hi@0bdx.com> (0bdx.com)/' *.json
sed -ix 's/: "ISC",/: "MIT",/' *.json
sed -ix 's/"main": "index.js"/"type": "module"/' *.json
rm package.jsonx
```
