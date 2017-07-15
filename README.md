# beautification

#### Shared Commands

Install packages.

```unix
yarn install
```

#### Project Specific Commands

Link to shared dot files.

```unix
ln -nfs ~/GitHub/rkiel/beautification/jsbeautifyrc.json .jsbeautifyrc
ln -nfs ~/GitHub/rkiel/beautification/jshintrc.json .jshintrc
ln -nfs ~/GitHub/rkiel/beautification/jshintignore.json .jshintignore

```

Hide shared dot files from Git.

```unix
echo .jsbeautifyrc >> .gitignore
echo .jshintrc >> .gitignore
echo .jshintignore >> .gitignore
```
