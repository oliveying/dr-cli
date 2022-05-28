## lerna 命令
```bash
lerna add -h
lerna create name ## 创建name的packages

lerna clean # 清空依赖
lerna add @dr-cli-dev/utils packages/core # 在core安装utils依赖
lerna bootstrap # 重新安装依赖

lerna link # 相互依赖

lerna exec -- rm -rf node_modules # 执行packages里的exec命令
lerna exec --scope my-component -- ls -la #执行指定命令

lerna run test # 执行每个packages下的npm 脚本

lerna publish
# lerna ERR! E402 You must sign up for private packages
"publishConfig": {
    "access": "public"
  }
```

## 拆分原则
根据模块功能拆分
* 核心模块 core
* 命令模块 commands
* 模型模块： models
* 工具模块： utils