<div align="center">

# SmartEdu Tools App

智慧教育公共服务平台（Smart Education of China）—— 中小学智慧教育平台 —— 资源下载工具

支持解析 PDF、PPT、MP3 及 MP4 等资源格式，支持本地预览、批量下载和资源归档

原生支持 Windows 和 macOS 操作系统

</div>

| <img width="447" src="https://github.com/user-attachments/assets/5723f099-b9b2-4561-a557-9b71fb5a5300" /> | <img width="447" src="https://github.com/user-attachments/assets/641a8f43-50c9-4ed5-9d64-355551fdafa3" /> |
| :---: | :---: |
| macOS | Windows |




## 开始使用

根据系统环境（`Windows`/`macOS`）选择对应版本，下载完成后无需安装，解压文件即可运行。

- 官方下载：[最新版本](https://github.com/vultur/SmartEdu-Tools-App/releases/latest)
- 备用地址：[网盘链接](https://pan.baidu.com/s/1PCzyFEekGdoB4wQW0w6r0A?pwd=0521)

## 功能特性

- 🤖 **极简操作**：自动解析资源链接，自动获取令牌，无需繁琐操作
- 📚 **同步更新**：实时获取平台最新资源，同步下载新学期教材版本
- 🔮 **全能解析**：支持 PDF/PPT/MP3/MP4 资源解析，自动解密数据
- ⚡️ **批量下载**：按学段、学科、版本、年级筛选资源，一键批量下载
- 🗂️ **资源归档**：自动识别资源目录结构，智能创建子文件夹分类归档
- 🖥️ **原生体验**：适配 Windows 和 macOS 操作系统，运行稳定流畅

## 选择版本

> [!TIP]
> ✅ 完全支持 / ⚠️ 部分支持 / ❌ 不支持

<table>
  <thead>
    <tr>
      <th width="180px">功能类别</th>
      <th width="285px">专业版（Pro）</th>
      <th width="285px">基础版（Lite）</th>
    </tr>
  </thead>
  <tbody>
    <tr align="center">
      <td>教材资源</td>
      <td>✅ 同步更新</td>
      <td>✅ 同步更新</td>
    </tr>
    <tr align="center">
      <td>令牌管理</td>
      <td>✅ 自动获取</td>
      <td>✅ 自动获取</td>
    </tr>
    <tr align="center">
      <td>资源分类</td>
      <td>✅ 所有资源</td>
      <td>⚠️ 电子教材</td>
    </tr>
    <tr align="center">
      <td>资源格式</td>
      <td>✅ 全部格式</td>
      <td>⚠️ PDF</td>
    </tr>
    <tr align="center">
      <td>批量下载</td>
      <td>✅ 支持</td>
      <td>❌ 不支持</td>
    </tr>
    <tr align="center">
      <td>资源归档</td>
      <td>✅ 支持</td>
      <td>❌ 不支持</td>
    </tr>
  </tbody>
</table>

## 常见问题

**如何手动获取令牌？**

> 1. 打开浏览器，访问「智慧教育公共服务平台」并登录个人账号：[点击前往](https://auth.smartedu.cn/uias/login)
> 2. 打开**开发者工具**，点击切换到**控制台**（`Console`）选项卡
>     - 按下快捷键 `F12` 或 `Ctrl+Shift+I`（Windows）/ `Cmd+Opt+I`（macOS）；
>     - 或右键点击页面空白处，选择**检查**或**审查元素**。
> 3. 复制以下代码，粘贴到**控制台**并按下**回车键**（`Enter`）：
>
>    ```js
>    (() => {
>       const authKey = Object.keys(localStorage).find(k => k.startsWith("ND_UC_AUTH"));
>       if (!authKey) return console.error("未找到令牌，请登录或刷新后重试！");
>       
>       const accessToken = JSON.parse(JSON.parse(localStorage.getItem(authKey)).value).access_token;
>       console.log("%c%s", "color: green; font-weight: bold", accessToken);
>     })();
>    ```
>
> 4. 复制控制台输出的访问令牌（**绿色文本**），在 **SmartEdu Tools** 主界面完成设置
> [!WARNING]
> 访问令牌存在过期可能性！若下载过程中提示`令牌过期或无效`，请重新获取并更新访问令牌即可。
