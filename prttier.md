#安装prettier

```
	局部安装
	npm install --save-dev --save-exact prettier
	# or globally
	全局安装
	npm install --global prettier
```
#配置
```
	在文件根目录建立.prettierrc.js文件:
	//.prettierrc.js文件中如下配置
	module.exports = {
	    semi: false,
	    singleQuote: true,
	}
```
	
#格式化某个文件
```
	prettier --write “src\index.js”
```