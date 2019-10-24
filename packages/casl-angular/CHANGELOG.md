# Change Log

All notable changes to this project will be documented in this file.

# [@casl/angular-v2.1.0](https://github.com/stalniy/casl/compare/@casl/angular@2.0.0...@casl/angular@2.1.0) (2019-07-01)


### Features

* **angular:** upgrades Angular and typescript ([08591f4](https://github.com/stalniy/casl/commit/08591f4)), closes [#158](https://github.com/stalniy/casl/issues/158) [#195](https://github.com/stalniy/casl/issues/195)

# [@casl/angular-v2.0.0](https://github.com/stalniy/casl/compare/@casl/angular@1.0.0...@casl/angular@2.0.0) (2019-02-10)


### Bug Fixes

* **packages:** increases peerDependency of [@casl](https://github.com/casl)/ability ([9f6a7b8](https://github.com/stalniy/casl/commit/9f6a7b8)), closes [#119](https://github.com/stalniy/casl/issues/119)


### Features

* **ability:** adds support for `manage` action ([d9ab56c](https://github.com/stalniy/casl/commit/d9ab56c)), closes [#119](https://github.com/stalniy/casl/issues/119)


### BREAKING CHANGES

* **ability:** `manage` is not anymore an alias for CRUD but represents any action.

Let's consider the next example:

```js
const ability = AbilityBuilder.define((can) => {
  can('manage', 'Post')
  can('read', 'User')
})
```

In @casl/ability@2.x the definition above produces the next results:

```js
ability.can('read', 'Post') // true
ability.can('publish', 'Post') // false, because `manage` is an alias for CRUD
```

In @casl/ability@3.x the results:

```js
ability.can('read', 'Post') // true
ability.can('publish', 'Post') // true, because `manage` represents any action
```

To migrate the code, just replace `manage` with `crud` and everything will work as previously.

# [@casl/angular-v1.0.0](https://github.com/stalniy/casl/compare/@casl/angular@0.4.1...@casl/angular@1.0.0) (2018-12-02)


### Bug Fixes

* **angular:** adds possibility to use angular module in lazy loaded routes ([0c7c3c1](https://github.com/stalniy/casl/commit/0c7c3c1))


### BREAKING CHANGES

* **angular:** Fixes #131

# [@casl/angular-v0.4.1](https://github.com/stalniy/casl/compare/@casl/angular@0.4.0...@casl/angular@0.4.1) (2018-11-11)


### Bug Fixes

* **angular:** makes `field` to be optional argument ([a3eec63](https://github.com/stalniy/casl/commit/a3eec63)), closes [#126](https://github.com/stalniy/casl/issues/126)

# [@casl/angular-v0.4.0](https://github.com/stalniy/casl/compare/@casl/angular@0.3.1...@casl/angular@0.4.0) (2018-11-11)


### Bug Fixes

* **angular:** converts source to typescript ([565936d](https://github.com/stalniy/casl/commit/565936d)), closes [#126](https://github.com/stalniy/casl/issues/126)
* **README:** changes links to [@casl](https://github.com/casl)/ability to point to npm package instead to git root [skip ci] ([a74086b](https://github.com/stalniy/casl/commit/a74086b)), closes [#102](https://github.com/stalniy/casl/issues/102)
* **semantic-release:** test ([cab3f4b](https://github.com/stalniy/casl/commit/cab3f4b)), closes [#94](https://github.com/stalniy/casl/issues/94)


### Features

* **react:can:** updates typescript declarations ([213dcde](https://github.com/stalniy/casl/commit/213dcde))

<a name="@casl/angular-v0.3.1"></a>
# [@casl/angular-v0.3.1](https://github.com/stalniy/casl/compare/@casl/angular@0.3.0...@casl/angular@0.3.1) (2018-07-02)


### Bug Fixes

* **package:** changes location of ES5M modules ([2b1ad4e](https://github.com/stalniy/casl/commit/2b1ad4e)), closes [#89](https://github.com/stalniy/casl/issues/89)

<a name="0.3.0"></a>
# 0.3.0 (2018-05-14)


### Features

* **angular:** supports per field abilities ([8268bb4](https://github.com/stalniy/casl/commit/8268bb4))



<a name="0.2.0"></a>
# 0.2.0 (2018-04-26)


### Features

* **angular:** adds typings ([98644ba](https://github.com/stalniy/casl/commit/98644ba)), closes [#38](https://github.com/stalniy/casl/issues/38)


<a name="0.1.0"></a>
# 0.1.0 (2018-03-23)


### Features

* **angular:** adds angular integration and tests, closes [#24](https://github.com/stalniy/casl/issues/24)
