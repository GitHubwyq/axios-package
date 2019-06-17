### 使用说明
#### 1、安装axios
> npm install axios

#### 2、建文件夹
> 一般会在项目的src目录中，新建一个request文件夹，然后在里面新建一个http.js和一个api.js文件。http.js文件用来封装我们的axios，api.js用来统一管理我们的接口。

#### 3、引入
> ①在main.js中引入http.js,并全局挂载它
```js
import axios from './request/http.js'     //引入http.js

Vue.prototype.$http = axios        //全局挂载封装的http.js
```
> ②在需要请求接口的地方引入api.js（当然你也可以全局挂载api.js）

#### 4、使用
```js
this.$http.get(api.接口名路径).then((data)=>{

}).catch((err) => {
    
})
```