# beautification

Install the repo

```unix
mkdir -p ~/GitHub/rkiel && cd $_
git clone git@github.com:rkiel/beautification.git
cd beautification
```

Choose between `eslint` and `jshint`.

#### jsbeautify

In your project, link to shared dot files.

```unix
ln -nfs ~/GitHub/rkiel/beautification/jsbeautifyrc.json .jsbeautifyrc
```

In your project, hide shared dot files from Git.

```unix
echo .jsbeautifyrc >> .gitignore
```

#### eslint

Install Atom package.

```unix
apm install linter-eslint
```

Install npm package.

```unix
yarn add --dev eslint
```

In your project, link to shared dot files.

```unix
ln -nfs ~/GitHub/rkiel/beautification/eslintrc.json .eslintrc
ln -nfs ~/GitHub/rkiel/beautification/eslintignore.json .eslintignore
```

In your project, link to shared dot files from Git.

```unix
echo .eslintrc >> .gitignore
echo .eslintignore >> .gitignore
```

#### jshint

Install Atom package.

```unix
apm install linter-jshint
```

Install npm package.

```unix
yarn add --dev jshint
```

In your project, link to shared dot files.

```unix
ln -nfs ~/GitHub/rkiel/beautification/jshintrc.json .jshintrc
ln -nfs ~/GitHub/rkiel/beautification/jshintignore.json .jshintignore
```

In your project, link to shared dot files from Git.

```unix
echo .jshintrc >> .gitignore
echo .jshintignore >> .gitignore
```
