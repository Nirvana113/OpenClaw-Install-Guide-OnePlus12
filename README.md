# 📱 OpenClaw Installation Guide - OnePlus 12

<div align="center">

**适用于 Android + Termux + GLM-4.7-Flash 免费方案**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Android](https://img.shields.io/badge/Platform-Android-green.svg)](https://www.android.com/)
[![Node.js](https://img.shields.io/badge/Node.js-22+-blue.svg)](https://nodejs.org/)
[![OpenClaw](https://img.shields.io/badge/OpenClaw-Latest-orange.svg)](https://docs.openclaw.ai)

[中文教程](教程.md) • [English Tutorial](教程-英文.md)

</div>

---

## 📖 简介

本教程详细介绍了如何在**一加12手机**上通过**Termux + proot-distro**安装 **OpenClaw**，并配置 **GLM-4.7-Flash** 免费大模型，最终实现通过 **Telegram** 与AI助手交互。

### ✨ 特点

- ✅ 完全免费（使用智谱AI GLM-4.7-Flash）
- ✅ 超长上下文（204800 tokens）
- ✅ 推理能力强
- ✅ Telegram无缝集成
- ✅ 本地运行，隐私安全

---

## 🎯 适用人群

- 一加12用户
- Android开发者
- 需要本地AI助手
- Telegram爱好者
- 科技爱好者

---

## 📋 快速开始

### 前提条件

- [ ] 一加12手机
- [ ] F-Droid应用商店
- [ ] Termux和Termux:API
- [ ] 科学上网环境
- [ ] 智谱AI账号
- [ ] Telegram Bot Token

### 安装步骤

1. **更新Termux环境**
   ```bash
   pkg update && pkg upgrade -y
   ```

2. **安装依赖**
   ```bash
   pkg install build-essential nodejs-lts git cmake python proot-distro -y
   ```

3. **安装Ubuntu容器**
   ```bash
   proot-distro install ubuntu
   proot-distro login ubuntu
   ```

4. **安装Node.js**
   ```bash
   curl -fsSL https://deb.nodesource.com/setup_22.x | bash -
   apt install -y nodejs
   ```

5. **安装OpenClaw**
   ```bash
   npm install -g openclaw@latest
   ```

6. **运行配置向导**
   ```bash
   openclaw onboard --install-daemon
   ```

7. **配对Telegram**
   ```bash
   openclaw gateway start
   openclaw pairing approve telegram YOUR_CODE
   ```

8. **启动Gateway**
   ```bash
   openclaw gateway start
   ```

9. **防止进程被杀死**
   ```bash
   termux-wake-lock
   ```

---

## 📚 详细教程

📖 **中文教程**：[教程.md](教程.md)

📖 **English Tutorial**：[教程-英文.md](教程-英文.md)

---

## ⚙️ 配置说明

### 智谱AI API配置

```json
{
  "agent": {
    "model": "glm-4.7-flash",
    "apiProvider": "custom",
    "apiBaseUrl": "https://open.bigmodel.cn/api/paas/v4"
  }
}
```

### Telegram Bot Token获取

1. 打开Telegram
2. 搜索 `@BotFather`
3. 发送 `/newbot`
4. 按提示创建Bot
5. 保存生成的Token

---

## 🔧 常见问题

### Q: 网络连接失败？

**A**: 检查科学上网，确保Termux有网络权限

### Q: Node.js安装失败？

**A**: 使用国内镜像源：
```bash
npm config set registry https://registry.npmmirror.com
```

### Q: proot网络权限问题？

**A**: 重新执行第6步的修复脚本

### Q: 模型无法调用？

**A**: 检查API Key，确认智谱AI账户有余额

---

## 🛡️ 防止进程被杀死

### Termux中

```bash
termux-wake-lock
```

### 手机系统设置

设置 → 应用 → Termux → 电池 → **无限制**

---

## 📊 性能参数

| 项目 | 参数 |
|------|------|
| **模型** | GLM-4.7-Flash |
| **上下文窗口** | 204800 tokens |
| **推理能力** | ✅ 支持 |
| **免费额度** | ✅ 完全免费 |
| **响应速度** | 快 |
| **支持语言** | 中文、英文等 |

---

## 🔄 更新日志

### v1.0.0 (2026-03-23)

- ✅ 初始版本发布
- ✅ 完整安装教程（中文+英文）
- ✅ Telegram集成配置
- ✅ GLM-4.7-Flash模型配置
- ✅ 常见问题解答
- ✅ MIT许可证

---

## 📚 相关链接

- [OpenClaw官方文档](https://docs.openclaw.ai)
- [智谱AI官网](https://open.bigmodel.cn)
- [Termux官方文档](https://wiki.termux.com)
- [F-Droid应用商店](https://f-droid.org)

---

## 🤝 贡献

欢迎提交Issue和Pull Request！

---

## 📄 许可证

本项目采用 [MIT License](LICENSE) 开源。

---

## 💬 支持

如有问题，请提交 [Issue](https://github.com/Nirvana113/OpenClaw-Install-Guide-OnePlus12/issues)

---

<div align="center">

**最后更新**：2026年3月23日

Made with ❤️ by [Nirvana113](https://github.com/Nirvana113)

</div>
