[English Introduction](./README_en.md)

# 简介

这是一个 Zotero 中能够运行的 JavaScript 脚本，它的作用是当你选中一个或者多个条目之后，能够从  dblp 网站或者 Google Scholar 上面自动获取搜索排列为第一条的搜索结果的 Bibtex 信息，并解析用以填充文献信息。

以下是两则数据安全性声明：

1. 为保证数据的安全性如果获取的条目的类型，与 Zotero 中原本的类型不一致，将会新建一个条目，并把相关信息、附件、标签都拷贝过去，但保留原条目不删除。
2. 除了作者、编辑的信息会直接覆盖，标题的信息不会覆盖之外，其他任何信息都是仅在原数据为空的情况下才引入 Bibtex 的信息，即不会覆盖原有的信息。

# 使用方式

## 无 Quicker 使用方式

1. 选中你想填充的文献条目
2. 点击“工具”-“开发者”-“Run JavaScript”
3. 将`main.js`代码复制粘贴进去
4. 再点击左上角“Run”按钮即可运行。
 
后续考虑做UI打包成 Zotero 右键插件。

## 有 Quicker 使用方式

如果你有Quicker，你可以直接使用我分享的动作：[传送门点这里~](https://getquicker.net/Sharedaction?code=e1553bba-54eb-41f0-2253-08dc1310ce90&fromMyShare=true)

Quicker 具体使用方式可以直接看动作页简介。

> 另外，如果你是新用户的话我的邀请码是 970091-5834，填邀请码之后再付费能够各增加三个月会员。

顺利的情况如下：
![success](imgs/success.png)

出现问题的情况如下：
![failed](imgs/failed.png)

# 待办

- [x] 支持更多 Bibtex 来源站
  - [x] DBLP
  - [x] Google Scholar
- [x] 整理代码，使用 Zotero 自带的解析 BibTex 功能
- [ ] 整理代码，使用 Zotero 的数据库操作精简复制条目的代码部分
- [ ] 整理代码，抽离并设计用户可配置项
- [ ] 做 UI，将其作为 Zotero 右键选项
- [ ] 打包成xpi插件