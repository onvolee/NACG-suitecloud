# SDF开发流程

nesuite账号使用SDF开发需要到"Setup > Company > Enable Features > SuiteCloud"路径下开启"SuiteCloud Development Framework"功能。
开启后即可使用 SuiteCloud cli, SuiteCloud vscode plugin等方式来执行导入、验证、部署等SDF操作。

## 项目结构

```json
src
|
|--FileCabinet
|  |--SuiteScripts // 存放netsuite script
|--Objects // 存放部署的netsuite script的record配置
|--deploy.xml // 部署配置, 执行project:validate, project:package, project:deploy会读取该配置
|--manifest.xml // 声明项目类型，"ACCOUNTCUSTOMIZATION" => 面向特定 netsuite 账号的定制项目
jest.config.js // 测试配置
AGENTS.md // 配置通用agent规范，如suitescript best pratices, suitescript workflow等.
suitecloud.config.js //
project.json // 认证别名,属于本地个人或ci环境
```

## cicd 

为满足suitecloud cli 3.2.0要求，需使用oauth2.0 认证。netsuite官方要求oauth2.0证书最多是2年一配置
