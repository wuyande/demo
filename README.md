# 持续集成使用报告

## 阿里云云效

### ci配置步骤

#### 前置条件: 
1. 已经创建好项目
2. 已经创建好代码仓库 支持的语言包括:
- Java
- NodeJS
- PHP
- Python
- Go
- 自定义镜像

#### 重点功能使用简介
1. 创建流水线 流水线支持一下种类:
2. 流水线触发条件存在三种方式：手动触发 自动触发 定时触发
3. 自动触发配置代码仓库
4. 支持以下输入源

![Image text](./report/jpg/流水线输入源支持列表.png)

5. github配置webhook后,github代码提交后会向云效发送POST请求，云效随后执行相应构建。
6. githubwebhook配置

![Image text](./report/jpg/githubwebhook配置.png)

7. 可以在github上配置什么时候触发云效的构建
8. 执行过程及结果，可以查看日志

![Image text](./report/jpg/构建结果.png)

9. 执行完成后可以下载产物 内容包含打包产物和启动脚本

![Image text](./report/jpg/下载.png)

#### 使用总结
##### 优点
1. 功能健全,可以满足手动触发构建某个分支，定期构建分支，代码提交构建分支的要求。
2. webhook配置说明不够详细。
3. 触发功能丰富可以解决各种场景。
4. 有一些构建后置任务可以配置。例如测试用执行红线，代码安全扫描以及安全规约扫描。

##### 缺点 
1. 代码只支持码云和阿里云代码
2. 虽然可以配置github自动触发但是，构建产物不能基于github代码构建。

## 2. 华为云

#### 基本步骤
1. 基本信息配置

2. 源代码配置

![Image text](./report/jpg/华为云源代码支持.png)

- 两点支持直接oauth一键认证github仓库。极其方便。赞！

3. 配置构建模板 华为云支持的

![Image text](./report/jpg/华为云模板1.png)

![Image text](./report/jpg/华为云模板2.png)

![Image text](./report/jpg/华为云模板3.png)

4. 配置构建

![Image text](./report/jpg/华为云构建配置.png)

- 可以修改构建指令(黑框部分)
- 可选工具版本

5. 配置结果上传配置

![Image text](./report/jpg/华为云上传构建.png)

- 支持直接下载构建包

6. 查看结果

![Image text](./report/jpg/华为云结果.png)

- 可以看日志
- 在页面直接下载结果包


