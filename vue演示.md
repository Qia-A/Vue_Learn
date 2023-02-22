# 搭建VUE项目的基本步骤

## 1、引入Vue.js

```html
<script src="https://cdn.jsdelivr.net/npm/vue@2.7.14"></script>
```

## 2、搭建Vue环境

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vue</title>
    <!-- 开发环境版本，包含了有帮助的命令行警告 -->
    <script src="js/vue.js"></script>
</head>
<body>
    <div id="app">

        {{message}}

        name : {{name}}

    </div>
</body>
<script>
    var app = new Vue({
      el: '#app',
      data: {       //这个里面写数据
        message: 'Hello Vue!',
        name: 'asdasd',
      },
      methods:{     //这个里面写函数
        
      },
      mounted(){    //当页面启动时，加载里面的东西
    
      }
    })
    </script>
</html>
```

打开网页查看，如果看到Hello Vue，说明VUE搭建成功。

## 3、获取input的数据

v-model="data里面的值"

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vue</title>
    <!-- 开发环境版本，包含了有帮助的命令行警告 -->
    <script src="js/vue.js"></script>
</head>
<body>
    <div id="app">

        <input v-model="value">
        {{value}}

    </div>
</body>
<script>
    var app = new Vue({
      el: '#app',
      data: {       //这个里面写数据
        value: '',
      },
      methods:{     //这个里面写函数
        
      },
      mounted(){    //当页面启动时，加载里面的东西
    
      }
    })
    </script>
</html>
```

## 4、控制dom元素的显示

v-show="填布尔值"

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vue</title>
    <!-- 开发环境版本，包含了有帮助的命令行警告 -->
    <script src="js/vue.js"></script>
</head>
<body>
    <div id="app">

        <div style="width: 200px;height:200px;background-color: red;" ></div>
        <div style="width: 200px;height:200px;background-color:aqua ;" v-show="show"></div>

    </div>
</body>
<script>
    var app = new Vue({
      el: '#app',
      data: {       //这个里面写数据
        value: '',
        show: true      //这里写true，代表显示，写false，消失
      },
      methods:{     //这个里面写函数
        
      },
      mounted(){    //当页面启动时，加载里面的东西
    
      }
    })
    </script>
</html>
```

## 5、Vue中的函数

Vue中的函数必须写在methods中

如果需要给按钮添加点击事件

  需要在按钮添加@click="methods中的函数名"

例如：<button @click="add">点我数字加一</button>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vue</title>
    <!-- 开发环境版本，包含了有帮助的命令行警告 -->
    <script src="js/vue.js"></script>
</head>
<body>
    <div id="app">

        <button @click="add">点我数字加一</button>
        {{count}}
    
    </div>
</body>
<script>
    var app = new Vue({
      el: '#app',
      data: {       //这个里面写数据
        count: 0
      },
      methods:{     //这个里面写函数
        add(){
           this.count++;    //methods里面的函数如果要调用data里面的数据，必须加个this
        }
      },
      mounted(){    //当页面启动时，加载里面的东西
        console.log('页面启动了')
      }
    })
    </script>
</html>
```

