# beautification

A generic project setup for JavaScrpt beautification.

## Installation

```unix
mkdir -p ~/GitHub/rkiel && cd $_
git clone git@github.com:rkiel/beautification.git
cd beautification
```

## Atom Setup

#### Install atom packages

```unix
apm install linter
apm install linter-ui-default
apm install linter-eslint
apm install prettier-atom
```

#### Update `~/.atom/config.cson`

```json
"prettier-atom":
  formatOnSaveOptions:
    enabled: true
    isDisabledIfNotInPackageJson: true
  prettierOptions:
    singleQuote: true
```


## Project Setup

`cd` into your project directory.

#### Install npm packages

```unix
yarn add --dev eslint
yarn add --dev prettier
```

#### Link shared dot files

```unix
ln -nfs ~/GitHub/rkiel/beautification/eslintrc.json .eslintrc
ln -nfs ~/GitHub/rkiel/beautification/eslintignore.json .eslintignore
```

#### Git ignore shared dot files

```unix
echo .eslintrc >> .gitignore
echo .eslintignore >> .gitignore
```

#### Add scripts to `package.json`

Use `sc` from  [rkiel/node-utilities](https://github.com/rkiel/node-utilities) or manually add to `scripts` section of `package.json`.
```unix
sc add e as eslint .
sc add p as prettier --single-quote --write '"!(build|node_modules)/**/*.js"' '"*.js"'
```
