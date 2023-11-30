# README

## Setup

```sh
pnpm i @yandongxu/eslint-config-vue eslint typescript -D
```

## Usage

```js
/* eslint-env node */
require("@rushstack/eslint-patch/modern-module-resolution")

/**
 * @type {import("eslint").Linter.Config}
 */
module.exports = {
  extends: [
    // ... other configs
    "@yandongxu/eslint-config-vue"
    "@yandongxu/eslint-config-prettier"
  ],
  rules: {
    'no-console': process.env.NODE_ENV === 'production' ? 'warn' : 'off',
    'no-debugger': process.env.NODE_ENV === 'production' ? 'warn' : 'off',
  },
  parserOptions: {
    ecmaVersion: 'latest',
  },
}
```
