# npm 包

注册 `npm`

本项目登录

```sh
Username: zenberge
Password:
Email: (this IS public) leesren@foxmail.com
Logged in as zenberge on https://registry.npmjs.org/.

```

第一次发包

```sh
npm publish
```

如果失败，可能是 你发的包 跟别人的冲突，换个名字即可 `package.json` 的 `name` 字段

更新包
1、本地更新版本号

比如我想来个 1.0.1 版本，注意，是最后一位修改了增 1，那么命令

`npm version patch` 回车就可以了；

比如我想来个 1.1.0 版本，注意，是第二位修改了增 1，那么命令

`npm version minor` 回车就可以了；

比如我想来个 2.0.0 版本，注意，是第一位修改了增 1，那么命令

`npm version major` 回车就可以了；

2、修改远端的版本,提交到远端 npm 中：

`npm publish`
