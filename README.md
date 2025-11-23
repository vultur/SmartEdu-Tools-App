<div align="center">


# SmartEdu Tools App

智慧教育公共服务平台（Smart Education of China）—— 中小学智慧教育平台 —— 资源下载工具

支持解析 PDF、PPT、MP3 及 MP4 等资源格式，支持本地预览、批量下载和文档整理

原生支持 Windows 和 macOS 操作系统

</div>


## 功能特性

- 🤗 **简单易用**：
  图形化界面设计，实时显示资源数量、文件大小及下载进度
  
- 🔗 **实时更新**：
  同步更新平台数据，本地预览资源信息，无需手动输入链接
  
- 📑 **自动解析**：
  支持 PDF、PPT、MP3 及 MP4 等资源格式，自动解析加密资源
  
- ⚡️ **批量下载**：
  支持选择学段、学科、版本、年级等资源目录，一键批量下载资源
  
- 🗂️ **文档整理**：
  支持根据资源目录自动创建子文件夹，方便查找和管理
    
- 💻 **跨平台运行**：
  提供 Windows 和 macOS 原生应用，运行稳定高效


## 使用说明

1. **下载应用程序**

   根据系统环境（`Windows`/`macOS`）选择下载对应的版本，点击查看：[最新版本](https://github.com/vultur/SmartEdu-Tools-App/releases)

   下载完成后点击即可运行，无需额外的安装步骤。

2. **获取访问令牌**
   
   首次运行并登录「智教中国通行证」获取访问令牌；后续无需重复登录，到期自动更新。

3. **开始下载资源**

   在主界面选择资源分类，即可实时获取、预览并下载资源。

> [!WARNING]
> 使用过程中遇到问题，请查阅：[常见问题](#常见问题)；若问题未解决或需要帮助，请提交：[问题反馈](https://github.com/vultur/SmartEdu-Tools-App/issues/new/choose)


## 版本对比

> [!TIP]
> 免费版已能满足个人日常需求，专业版更适合教育机构、教师等高频使用者。
>
> ✅ 完全支持 / ⚠️ 部分支持 / ❌ 不支持

| 功能类别 | 免费版 | 专业版 |
| --- | --- | --- |
| 资源数据 | ✅ 实时更新| ✅ 实时更新 |
| 下载速度 | ✅ 高速下载 | ✅ 高速下载 |
| 资源分类 | ⚠️ 基础类别（电子教材） | ✅ 全部类别（教材、课件、听力、视频课程、基础性作业等） |
| 资源格式 | ⚠️ 基础格式（PDF） | ✅ 全部格式（PDF、PPT、MP3、MP4等） |
| 令牌管理 | ⚠️ 手动获取 | ✅ 自动获取，到期自动更新 |
| 内容水印 | ⚠️ 有水印 | ✅ 无水印 |
| 批量下载 | ❌ 不支持 | ✅ 支持（按资源目录） |
| 文档整理 | ❌ 不支持 | ✅ 支持（按资源目录） |
| 技术支持 | ❌ 无（社区支持） | ✅ 有（支持定制） |

> [!IMPORTANT]
> **免费版**用户如需获取`全部类别`或`全部格式`的资源，请前往：[SmartEdu-Textbook](https://github.com/vultur/SmartEdu-Textbook)
>
> 根据指南获取网盘分享链接，即可免费下载所有教材资源。


## 常见问题

**如何手动获取令牌？**

> 1. 打开浏览器，访问「智慧教育公共服务平台」并登录个人账号：[点击前往](https://auth.smartedu.cn/uias/login)
> 2. 打开**开发者工具**，点击切换到**控制台**（`Console`）选项卡
>     - 按下快捷键 `F12` 或 `Ctrl+Shift+I`（Windows）/ `Cmd+Opt+I`（macOS）；
>     - 或右键点击页面空白处，选择**检查**或**审查元素**。
> 3. 复制以下代码，粘贴到**控制台**并按下**回车键**（`Enter`）：
>    ```js
>    (() => {
>       const authKey = Object.keys(localStorage).find(k => k.startsWith("ND_UC_AUTH"));
>       if (!authKey) return console.error("未找到令牌，请登录或刷新后重试！");
>       
>       const accessToken = JSON.parse(JSON.parse(localStorage.getItem(authKey)).value).access_token;
>       console.log("%c%s", "color: green; font-weight: bold", accessToken);
>     })();
>    ```
> 4. 复制控制台输出的访问令牌（**绿色文本**），在 **SmartEdu Tools** 主界面完成设置

> [!WARNING]
> 访问令牌存在过期可能性！若下载过程中提示`令牌过期或无效`，请重新获取并更新访问令牌即可。


<br />
<br />

