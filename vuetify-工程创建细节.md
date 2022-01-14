#因为会出现eslint问题,所以vue创建工程的步骤如下

## 通过vue-cli脚手架,创建vue工程
```
	1. vue create test
	2. 选择manually select features (自定义选择特性) 从而可以配置eslint
	3. 选择Vuex和Router即可
	4. 选择2.x
	5. history (no)
	6. ESLint + Prettier (代码更漂亮)
	7. In package.json (默认的配置文件,eslint等配置写入该文件中)
	8. Save this as a preset for future project? (no) 意思是该配置可以其它工程使用
```
## 添加vuetify组件
```
	1. cd test
	2. vue add vuetify
```
## 启动
```
	1. npm run serve
```