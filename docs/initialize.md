# How to setup a new project with Husky

## Documentation
[Husky](https://typicode.github.io/husky/#/)  
[Commitzen](https://commitizen-tools.github.io/commitizen/)  
[Commitlint](https://commitlint.js.org/#/)  

## How to

### Install packages

```sh
npm install -D -g commitizen
npm install -D husky
npm install -D @commitlint/config-conventional @commitlint/cli
```

### Configure Commitzen

```sh
//npm
commitizen init cz-conventional-changelog --save-dev --save-exact

//yarn
commitizen init cz-conventional-changelog --yarn --dev --exact
```

### Configure commitlint to use conventiona config

```sh
echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js
```

### Configure Husky

#### Using Commitlint to verify all your commits
```sh
//yarn
yarn husky add .husky/commit-msg 'yarn commitlint --edit $1'

//npm
npx husky add .husky/commit-msg 'npx --no -- commitlint --edit'
```

#### Using commitzen on git commit
```sh
//yarn
yarn husky add .husky/prepare-commit-msg ''

//npm
npx husky add .husky/prepare-commit-msg ''
```

```sh
echo 'if cat $1 | grep -q "^#[A-Za-z ]*"; then\n    exec < /dev/tty && git cz --hook || exit 1\nfi' >> .husky/prepare-commit-msg
```

#### Force test run on push
```sh
//yarn
yarn husky add .husky/pre-push 'yarn test'

//npm
npx husky add .husky/pre-push 'npm test'
```