# vitis-server

node 的版本是 14.17.0

## 前置准备

### 安装 MongoDB

启动项目前在本地主机安装 MongoDB，同时让 MongoDB 实例运行在 27017 端口。

### 环境变量配置文件

在项目更目录创建 env.config.json，文件内容如下：

```json
{
    // 你的 gitlab PRIVATE-TOKEN
    "GITLAB_TOKEN": "xxxx",
    "GITLAB_URL": "https://gitlab.com",
    "MONGODB_URL": "mongodb://localhost:27017/vitis",
}
```

## 启动

```dotnetcli
npm i
npm run server
```

## 兼容性

1. bcrypt: 如果在安装依赖的时候有 node-pre-gyp 相关的错误，请在 https://github.com/kelektiv/node.bcrypt.js 找解决办法。

## 《低代码平台开发实践：基于React》

2020年初，为了加速重构遗留系统，我在任职的公司落地了低代码，当时的低代码及其简陋，不足为道，但派上了用场，我们只有5个前端工程师，在一个季度内，搭建了200+个页面。回忆起当时的方案，大概存在以下5个问题：
1. 搭建完成的应用无法独立部署
2. 无渲染沙箱，当处于编辑态时，画布无纯净的运行环境
3. 无组件市场，低代码设计器能使用的组件全部写死在项目内
4. 用来描述低代码应用的Schema无版本管理，无法查看以前保存的版本。
5. 开发人员无法对搭建完成的应用二次开发。
2021 年底，机械工业出版社的图书编辑邀请我写一本与开发低代码相关的图书，今日，业已成书。本书一一解决了上述 5 个问题，同时涉及业务场景的需求分析，从开发技术层面来讲，读者将了解到下面这 5 个方面的内容：
   
1）JSON Schema保存到Git仓库中，它不影响线上运行的低代码应用，只用于APP各版本的预览和重新编辑。

2）线上运行的应用与JSON Schema脱钩，即便低代码平台停止服务，线上的APP依然能正常运行。

3）引入渲染沙箱，设计器和渲染器位于不同的Frame，此时画布拥有纯净的运行环境。

4）设计组件规范，开发脚手架，其用于开发、调试和上传低代码组件，这使设计器能使用丰富的组件去开发应用，同时让低代码组件和低代码平台解耦。

5）开发低代码平台所需的基础设施，包括GitLab CI/CD、npm私有库，LDAP账号管理系统等。

本书将分为4大部分，其中第3部分介绍开发低代码平台涉及的各个方面，这部分难度最大。如果你是一名经验丰富的软件工程师并且对低代码已有了解，建议从第4章开始；但是，如果你对低代码了解得不多，请一定从第一章的基础理论知识开始学习。

第一部分是基础篇，只包含一章，它介绍后续章节使用的理论知识，涉及的知识点有React Context API、React Hooks、React Ref、Mobx和MongoDB等，要想在本地运行本图书介绍的低代码平台，你需要在自己电脑上下载MongoDB。

第二部分为需求分析篇，包含两章，它介绍低代码平台开发的应用要满足哪些需求，同时也介绍低代码平台的功能。

第三部分为实战篇，包含五章，是本图书的重点，介绍如何开发低代码平台，其中展示了大量的代码示例，涉及的内容有低代码架构策略、低代码组件、设计器、渲染器和代码生成器。

第四部分为基础设施篇，只包含一章。低代码平台用于创建应用程序，它本身也是应用程序，值得一提的是，它对研发体系的要求相当高。如果你手上没有一套完善的研发体系，涵盖代码托管、CI/CD、CDN，npm私有库等部分，那么妄谈开发低代码平台。基础设施篇涉及的内容有，如何使用GitLab CI/CD建立持续部署 pipeline、如何搭建npm私有库，如何搭建LDAP账号管理系统等。
本图书提供了7个开源项目，全部源文件可以从https://github.com/react-low-code下载。

对《低代码平台开发实践：基于React》感兴趣的朋友可在[京东购买](https://item.jd.com/14012127.html)，也可通过我的微信微信公众号——前端知识小站联系到我。

![](./WechatIMG78.jpg)

