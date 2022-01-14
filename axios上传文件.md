#axios上传文件
```
https://www.jianshu.com/p/b3b47ea94007
<template>
  <div id="app">
    <input id="inputElement" name="file" type="file" accept="image/png, image/gif, image/jpeg"  />
    <button @click="upload">上传</button>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      file: null
    };
  },
  methods: {
    upload() {

      let inputElement = document.getElementById("inputElement")
      let file = inputElement.files[0];

      let param = new FormData(); // 创建form对象
      param.append("file", file); // 通过append向form对象添加数据

      param.append("chunk", "别的数据"); // 添加form表单中其他数据
      console.log(param.get("file")); // FormData私有类对象，访问不到，可以通过get判断值是否传进去

      let config = {
        headers: { "Content-Type": "multipart/form-data" }
      };

      axios.post("http://192.168.31.253:8080/upload", param, config);
    }
  }
};
</script>
```