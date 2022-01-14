#uniapp配置eslint

```
https://www.cnblogs.com/qinyuandong/p/13649904.html
vue add @vue/eslint (报错)

添加package.json
1"globals": {
2    "swan": "readonly",
3    "wx": "readonly",
4    "uni": "readonly"
5}

(版本过低)
https://segmentfault.com/a/1190000022743571
npm i eslint babel-eslint eslint-plugin-vue husky lint-staged prettier @vue/eslint-config-prettier eslint-plugin-prettier -D


npm install eslint --save-dev
https://www.npmjs.com/package/eslint

https://uniapp.dcloud.io/quickstart-cli
npm i @types/uni-app -D
npm i eslint@lastest
```