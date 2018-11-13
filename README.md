### 原生js插件 全屏展示图片，并且提供两种形式的图片链接

### 样式依赖于bootstrap

### 实用地址[地址](https://blog.liantao.me/jsWaterfall)

### 用法：

首先引入css、js:
 <!-- bootstrap -->
<link href="https://cdn.bootcss.com/twitter-bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet">
<link href="css/fullScreen.css" rel="stylesheet">
<script src="js/fullScreen.js"></script>

添加html:
```html
    <div id="fullScreen">
        <div id="fullScreen_popup_close">
            <!-- <button type="button" class="close" aria-label="Close"></button> -->
            <span class="glyphicon glyphicon-remove" aria-hidden="true"></span>
        </div>
        <!-- 弹窗-->
        <div id="fullScreen_popup">
            <!-- 关闭按钮 -->
            <div class="bg"><img src="" alt=""/></div>
            <!-- 展示图片地址栏 -->
            <div class="url_info">
                <div class="url_info_box">
                    <div class="input-group">
                        <span style="width:140px" class="input-group-addon">img url:</span>
                        <input style="width:660px" type="text" class="form-control" id="img_show_url" aria-describedby="basic-addon3">
                    </div>
                    <div class="input-group">
                        <span style="width:140px" class="input-group-addon">markdown img url:</span>
                        <input style="width:660px" type="text" class="form-control" id="markdownimg_show_url" aria-describedby="basic-addon3">
                    </div>
                </div>
            </div>
        </div>
    </div>
```

添加js:
```javascript
        //获取图片
    var imgs = document.getElementById("id").getElementsByTagName("img");
        //传递一个图片对象数组即可
        doFullScreen(imgs);
```
**只需要把一个图片数组给予 `doFullScreen`方法调用即可**

demo:
```html
<!DOCTYPE html>
<html lang="zh-cn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <!-- bootstrap -->
    <link href="https://cdn.bootcss.com/twitter-bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet">
    <link href="css/fullScreen.css" rel="stylesheet">
    <title>js full screen</title>
</head>
<style>
        .container {
            width: 600px;
            margin: 0 auto;
        }
        .container img{
            margin-right: 5%;
            margin-bottom: 30px;
            float: left;
        }

</style>
<body>
    <div id="container" class="container">
            <img src="images/0.jpg" alt=""/>
    </div>
   
    <div id="fullScreen">
        <div id="fullScreen_popup_close">
            <!-- <button type="button" class="close" aria-label="Close"></button> -->
            <span class="glyphicon glyphicon-remove" aria-hidden="true"></span>
        </div>
        <!-- 弹窗-->
        <div id="fullScreen_popup">
            <!-- 关闭按钮 -->
            <div class="bg"><img src="" alt=""/></div>
            <!-- 展示图片地址栏 -->
            <div class="url_info">
                <div class="url_info_box">
                    <div class="input-group">
                        <span style="width:140px" class="input-group-addon">img url:</span>
                        <input style="width:660px" type="text" class="form-control" id="img_show_url" aria-describedby="basic-addon3">
                    </div>
                    <div class="input-group">
                        <span style="width:140px" class="input-group-addon">markdown img url:</span>
                        <input style="width:660px" type="text" class="form-control" id="markdownimg_show_url" aria-describedby="basic-addon3">
                    </div>
                </div>
            </div>
        </div>
    </div>
    <script src="js/fullScreen.js?version=6999"></script>
    <script>
        //获取图片
        var imgs = document.getElementById("container").getElementsByTagName("img");
        //传递一个图片对象数组即可
        doFullScreen(imgs);

    </script>
    
</body>
</html>
```
