<div align="center">

# 🧭 Browser v2ray Runner(浏览器 v2ray 运行器)

**只在你的浏览器里运行代理 — 系统上的其他一切都保持原样**

![Windows](https://img.shields.io/badge/Windows-0078D6?logo=windows&logoColor=white)
![Chrome](https://img.shields.io/badge/Chrome-4285F4?logo=googlechrome&logoColor=white)
![Edge](https://img.shields.io/badge/Edge-0078D7?logo=microsoftedge&logoColor=white)
![Firefox](https://img.shields.io/badge/Firefox-FF7139?logo=firefoxbrowser&logoColor=white)
![Manifest V3](https://img.shields.io/badge/Manifest-V3-6f42c1)

[🇬🇧 English](README.en.md) · [🇮🇷 فارسی](README.md) · [⬇️ 从 Releases 下载](../../releases)

</div>

---

⚡ 只在浏览器内运行你的代理配置(VLESS、VMess、Trojan、Shadowsocks、SOCKS5)—— 没有沉重的后台常驻程序,不修改任何系统级设置。关掉扩展,一切立刻恢复原状。

## 💠 这是什么?

一个浏览器扩展(Windows 上的 Chrome、Edge、Firefox):读取你的代理链接,并**只把这一个浏览器的流量**通过代理转发。你电脑上的其他任何东西(其他应用、其他浏览器)都不受影响。

## 🚀 安装

安装分两部分:⬇️ 安装扩展,以及 🔧 对扩展所需的一个小型本地辅助程序做一次性设置。

### 第一步 — 下载并安装扩展

**🦊 Firefox:**
扩展已发布在 Firefox 官方附加组件商店,通过下面的链接直接安装即可:

👉 **[从 Firefox Add-ons 安装](https://addons.mozilla.org/en-US/firefox/addon/browser-v2ray-runner/)**

**🟦 Microsoft Edge:**
扩展同样已发布在 Edge 官方附加组件商店,通过下面的链接直接安装即可:

👉 **[从 Microsoft Edge Add-ons 安装](https://microsoftedge.microsoft.com/addons/detail/dmcfmgmajoikndpifnlggabbblggfppk)**

**🌐 Google Chrome:**
Chrome 版本尚未发布到 Chrome 网上应用店,需要手动安装:
1. 打开本仓库的 **[Releases](../../releases)** 页面,找到最新版本,下载并解压 `browser-v2ray-runner-chrome.zip`
2. 打开 `chrome://extensions`
3. 打开右上角的"开发者模式"
4. 点击"加载已解压的扩展程序",选择刚才解压出来的文件夹

### 第二步 — 设置本地辅助程序 🔧

首次安装扩展时,会自动打开一个新标签页引导你完成设置:

1. 🌍 选择语言(英语/波斯语)
2. 📥 下载一个小文件(`install.bat`)并双击运行
3. 👀 弹出的窗口会准确显示它准备下载的内容(文件名和大小),并等待你确认
4. ✅ 完成后,回到扩展那个标签页 —— 它会自动检测到一切,随即可用

> 🔒 **该安装程序只影响你自己的 Windows 用户账户** —— 不需要管理员权限,除了一个文件夹(`%LOCALAPPDATA%\V2rayExtHost`)之外,不会有任何改动。

> ⚠️ **如果 Windows 弹出 SmartScreen 警告:** 点击"更多信息",然后"仍要运行"。这个警告仅说明文件没有数字签名,并不代表文件有问题。你可以直接打开文件本身,查看它究竟做了什么。

## 🌌 如何使用

1. 点击浏览器工具栏上的扩展图标
2. 在输入框中粘贴配置链接(`vless://...`、`trojan://...` 等)或订阅链接,点击"添加" —— 它会自动识别类型
3. 点击任意配置旁的"连接" —— 图标变为 🟢 绿色,并显示你的出口 IP 和国家/地区
4. 再次点击同一个按钮即可断开

**✨ 其他功能:**
- 📡 **订阅(Subs)** 标签页:管理订阅链接(自动刷新配置列表)。已内置一个默认订阅 —— 可随时删除或修改
- ⚡ 批量测速:一次测试多个配置的速度(点击测试按钮)
- 🔀 按最近添加、速度或名称排序配置
- 🎨 在 **设置(Settings)** 标签页中切换语言和主题色

## ❓ 常见问题

**这会影响我的整个系统吗?**
不会。只有安装了该扩展的那个浏览器,其流量才会通过代理转发。其他应用和其他浏览器(如果你没有在那里安装它)完全不受影响。

**为什么需要一个单独的辅助程序?**
出于安全原因,浏览器不允许扩展直接运行代理这类网络进程。这个小程序(实际上就是代理引擎本身 —— [sing-box](https://github.com/SagerNet/sing-box))负责完成这项工作,并且只通过一条安全的本地通道与该扩展通信。

**带插件(如 v2ray-plugin)的 `ss://` 链接能用吗?**
目前还不能。

**可以同时连接多个配置吗?**
只能同时连接一个 —— 连接新配置会自动断开上一个。

---

🛠️ 技术细节、架构以及维护者/开发说明,请参阅 [DEVELOPMENT.md](DEVELOPMENT.md)。

## 📄 许可证与署名

本项目基于 [Apache License 2.0](LICENSE) 授权。你可以自由使用、修改和再分发本项目,但**必须署名原作者([hamedcode](https://github.com/hamedcode))并链接到源仓库**:请在副本或衍生作品中保留 [NOTICE](NOTICE) 文件,并标注你修改过的文件。隐私政策请参阅 [PRIVACY.md](PRIVACY.md)。
