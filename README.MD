# project_workflows

托管了很多开箱即用的 ci 配置，用于 github action，为[project_tool](https://github.com/seho-code-life/project_tool)提供安装支持，你可以使用这个工具，来可视化的添加 ci 配置文件并且轻松的管理 workflows 版本

#### 你可能需要准备的仓库环境变量

| 键名                      | 用途                                                                      |
| ------------------------- | ------------------------------------------------------------------------- |
| NPM_AUTH_TOKEN            | NPM 包管理 自动发布需要配置的环境变量 [查看](src/npm-publish.yml)         |
| QQ_UPLOAD_TOKEN           | QQ 小程序自动发布版本需要配置的环境变量 [查看](src/build-mp-qq.yml)       |
| WEIXIN_UPLOAD_PRIVATE_KEY | 微信 小程序自动发布版本需要配置的环境变量 [查看](src/build-mp-weixin.yml) |
| OSS_ACCESS_KEY_ID         | OSS 自动发布版本需要的 oss id [查看](src/release-oss.yaml)                |
| OSS_ACCESS_KEY_SECRET     | OSS 自动发布版本需要的 oss secret [查看](src/release-oss.yaml)            |
| GITEE_PRIVATE_KEY         | 同步仓库信息到 gitee 需要的 private key [查看](src/sync2gitee.yml)        |
| GITEE_TOKEN               | 同步仓库信息到 gitee 需要的 token [查看](src/sync2gitee.yml)              |

你需要仔细阅读每一个 yml 的配置，因为这可能与你的程序冲突，在 yml 文件中提供了很多注释说明和参考资料，这可能会帮助你完善 CI

#### 如何设置仓库环境变量?

github 仓库 -> setting -> secrets -> New repository secret
