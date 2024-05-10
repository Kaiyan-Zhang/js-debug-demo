### `feat: init`

.vscode/launch.json 是用的是 vscode 默认的模板，叫"Node.js"

### `feat: src`

注意`launch.json`的`program`字段

### `feat: module`

指定了`package.json`的`type`为`module`

### `feat: attach`

在`launch.json`中点右下角`Add Configuration`（将 vim 切换成 input 模式），然后选择`Node: Attach`，就可以创建一个新的 Config。

然后在终端执行

```
node --inspect-brk index.js
```

我们会看到 node 在等待 9229 端口的连接。

此时在 vscode 的侧边栏找到 debug，将脚本切换成刚刚创建出来的`Attach`，然后点击小三角运行，就可以看到程序在第一行停住了。

### `feat: js debug terminal`

直接`Cmd + Shift + P`，输入`Debug: Create JavaScript Debug Terminal`，会得到一个终端。在这个终端里面直接运行

```
node src/index.js
```

就可以触发 debug。

这个是最简单的办法。

### `feat: auto attach`

`Cmd + Shift + P`，搜索`Toggle Auto Attach`。

不过这个要求有`launch.json`。没有上一种简单。
