# VS Code Vim 插件使用说明

以下教程基于 macOS M1 版本：

## 自动切换中英文输入法

第一步：前往下载 [im-select](https://github.com/daipeihust/im-select#installation) 指令，放置到登录用户的 bin 文件夹，以我的 bin 文件夹路径为例：

```bash
/Users/liang/.local/bin
```

`liang` 是的我当前 Mac 的登录用户。

第二步：打开 VS Code 设置的 json 文件，追加以下设置项：

```json
  "vim.autoSwitchInputMethod.defaultIM": "com.apple.keylayout.US",
  "vim.autoSwitchInputMethod.enable": true,
  "vim.autoSwitchInputMethod.obtainIMCmd": "/Users/liang/.local/bin/im-select",
  "vim.autoSwitchInputMethod.switchIMCmd": "/Users/liang/.local/bin/im-select {im}",
  "vim.useSystemClipboard": true,
```

注意将 `obtainIMCmd` 和 `switchIMCmd` 的路径修改为自己当前电脑中的路径。

## 报错 permission denied 解决方案

原因：文件缺少可执行权限，使用 `chmod` 修改文件权限。

```bash
chmod x+u [文件路径]
chmod x+u /Users/liang/.local/bin/im-select
```

chmod 是权限管理命令 change the permissions mode of a file 的缩写。

`u` 代表所有者，`x` 代表执行权限，`+` 表示增加权限。
