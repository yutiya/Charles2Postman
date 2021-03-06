# Charles2Postman

recommend: [China-Gitee](https://gitee.com/liyinchi/Charles2Postman)，[Other-Github](https://github.com/liyinchigithub/Charles2Postman)

功能说明
===
```
测试小伙伴，经常使用Charles抓取数据包，但要将数据包内容复制到postman这是是一件费时费力的事情。

Charles2Postman可以帮助你，批量将Charles导出的抓包请求响应数据文件，快速转成支持导入postman格式，

让你在没有restful API设计文档情况下，快速构建postman客户端请求脚本，无需再一个个参数复制粘贴，节省时间。

```
支持基于http、https协议请求，请求数据类型支持urlencoded、json、form-data、html

版本
===

```
charles 版本 4.2.6

postman 版本 7.12.0

node 版本 大于v8.11.4
```


感谢[guohao0328](https://github.com/guohao0328)提出的第一个bug

环境
===

下载并安装nodejs
```
https://nodejs.org/en/
```

使用
===

进入目录

```
cd charles2postman
```
安装依赖
```
npm install
```

使用charles抓包工具
---

#### 将抓包内容，从charles中导出

![img](./static/image/导出文件.jpg)

>注意：导出请求格式为:JSON Session File（.chlsj），保存至Charles2Postman目录下File文件夹中。

#### 选择导出格式为".chlsj"

![img](./static/image/导出文件到File.jpg)


#### 将导出文件，保存至File文件夹中

![img](./static/image/导出文件到File例子.jpg)

>注意：File文件下面，不要放入其他格式的文件，仅能存放charles导出.chlsj格式文件，否则解析会出错。

开始转换
---

#### 方式一：
双击run.bat文件

![img](./static/image/windows双击bat文件.jpg)

#### 方式二：

```
npm run start

```
![img](./static/image/开始转换.jpg)

或

```
sudo sh run.sh
```


输出文件
---

转换结果，生成在outputFile目录下

```
./outputFile/postman_collection.json
```
![img](./static/image/转换后文件输出位置.jpg)

将转换结果，导入postman
---

将这个postman_collection.json导入postman中

![img](./static/image/将postman_collection.json导入postman中.jpg)


最终效果
---
![img](./static/image/最终效果.jpg)

>对你有所帮助的话，记得start下项目，谢谢你的支持
