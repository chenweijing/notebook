#添加axiox
```
http://www.axios-js.com/zh-cn/docs/vue-axios-plugin.html

npm install --save axios vue-axios

main.js 入口文件
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'

Vue.use(VueAxios, axios)

你可以按照以下方式使用:

Vue.axios.get(api).then((response) => {
  console.log(response.data)
})

this.axios.get(api).then((response) => {
  console.log(response.data)
})

this.$http.get(api).then((response) => {
  console.log(response.data)
})
```
#不用插件做法
```
https://blog.csdn.net/qq_36995521/article/details/115223647
```