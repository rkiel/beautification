# beautification

A generic project setup for JavaScript beautification.

## Installation

```unix
mkdir -p ~/GitHub/rkiel && cd $_
git clone git@github.com:rkiel/beautification.git
cd beautification
```

## Project Setup

`cd` into your project directory.

#### Install npm packages

```unix
yarn add --dev eslint
yarn add --dev prettier
yarn add --dev pre-commit
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
sc init
sc add e as eslint .
sc add pre-commit-eslint as eslint .
sc add p as prettier --single-quote --jsx-bracket-same-line --write '"!(build|node_modules)/**/*.js"' '"*.js"'
sc add pre-commit-prettier as prettier --single-quote --jsx-bracket-same-line --list-different '"!(build|node_modules)/**/*.js"' '"*.js"'
```

#### Add pre-commit to `package.json`

```json
"pre-commit": [
  "pre-commit-prettier",
  "pre-commit-eslint"
]
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
    jsxBracketSameLine: true
    singleQuote: true
```
