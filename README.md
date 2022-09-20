# DShanESP32 docs

百问网ESP32学习站点文档仓库。

# 参与文档修改

将本仓库 fork 到你的账号后，进行修改检查后提交pr到本仓库。

## 提交格式

提交的格式是： **`开发板名称(修改的部分): 修改描述`**

比如你修改的是 DShanMCU-Mio 中的 Arduino 部分的第一章，可以这样写：  

```shell
DShanMCU-Mio(Arduino): update chapter1
```

## 预览修改

如果需要预览修改的结果，可以按照下面的说明进行操作：

### windows

如果你是windows用户:

1. 先前往这里下载 nodekjs: [https://nodejs.org/en/download](https://nodejs.org/en/download/)
2. 进入到clone本仓库到本地之后的仓库根目录，在 **文件资源管理器** 的地址栏中输入 `cmd` 然后按回车进入到控制台
3. 先执行 `node -v` 和 `npm -v` 如果出现版本信息就是正常状态，然后看下一步
4. 执行 `npm i docsify-cli -g` 等待 **docsify** 安装完成之后再看下一步
5. 执行 `docsify serve ./` 按照提示在浏览器输入地址访问预览页面(一般是 `http://localhost:3000`)

之后如果在需要预览的时候，只需要进入到本仓库的根目录，然后执行 `docsify serve ./` 即可查看预览。

### linux

如果你是linux用户：

1. 安装 npm
2. 执行 `npm i docsify-cli -g` 等待 **docsify** 安装完成
3. 进入到clone本仓库到本地之后的仓库根目录
4. 执行 `docsify serve ./` 按照提示在浏览器输入地址访问预览页面(一般是 `http://localhost:3000`)

之后如果在需要预览的时候，只需要进入到本仓库的根目录，然后执行 `docsify serve ./` 即可查看预览。