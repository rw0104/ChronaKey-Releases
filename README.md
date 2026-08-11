# ChronaKey Releases

**想要一个不用登录账号、不会把 2FA 密钥传到云端的身份验证器？这就是 ChronaKey。**

ChronaKey 可以扫码、读取二维码图片或手动输入密钥，为 GitHub、Google、Microsoft 等支持
标准 TOTP/HOTP 的服务生成验证码。二维码、密钥和加密备份都由客户端在你的设备上处理。

## 立即下载

| 你的设备 | 下载 | 安装提醒 |
| --- | --- | --- |
| Android 手机 | [下载正式签名 APK](https://github.com/rw0104/ChronaKey-Releases/releases/download/v0.1.0-alpha.1/ChronaKey-Android-release.apk) | 已安装 Debug 版时需先备份并卸载旧版 |
| Windows 10/11 x64 | [下载 Windows 安装程序](https://github.com/rw0104/ChronaKey-Releases/releases/download/v0.1.0-alpha.1/ChronaKey-Windows-x64-unsigned-setup.exe) | 当前未签名，可能出现 SmartScreen 提示 |

👉 [查看版本说明和全部下载文件](https://github.com/rw0104/ChronaKey-Releases/releases/tag/v0.1.0-alpha.1)

> 当前是 Alpha 测试版。先用测试账户体验，不要立即迁移唯一一份生产 2FA 密钥；
> 请保留原验证器和恢复码。

## 你可以用它做什么

- 用相机扫描 2FA 二维码。
- 从截图或二维码图片中添加账户。
- 粘贴 `otpauth://` URI 或输入 Base32 密钥。
- 使用 TOTP/HOTP 验证码。
- 把账户保存在本地加密 Vault 中。
- 导出加密备份，在其他 ChronaKey 客户端恢复。

## 为什么是本地运行

ChronaKey 当前不提供账号系统、云同步、广告或遥测。正式客户端不依赖远程页面，也不会把
二维码和 OTP 密钥上传到服务器。你可以自行决定如何保管和转移加密备份。

## 平台进度

| 平台 | 当前状态 |
| --- | --- |
| Android | 已提供 ChronaKey Release 证书签名 APK |
| Windows | 已提供 x64 NSIS 测试安装程序，尚未做 Authenticode 签名 |
| Linux | `.deb`、`.AppImage` 等待 Linux runner 恢复后构建 |
| macOS | Universal `.dmg` 等待真实 macOS 构建与验证 |
| iOS | 需要 Apple 签名，将通过 TestFlight 或登记设备渠道测试 |

## 如何核对下载文件

请只从本仓库的 [GitHub Releases](https://github.com/rw0104/ChronaKey-Releases/releases)
下载，并核对版本附带的 `SHA256SUMS`：

```powershell
Get-FileHash .\ChronaKey-Windows-x64-unsigned-setup.exe -Algorithm SHA256
```

```bash
sha256sum -c SHA256SUMS
```

## 安全原则

- 安装前核对文件名、版本和 SHA-256。
- Alpha 阶段不要迁移唯一一份生产 2FA 密钥。
- 不要在 Issue、截图或日志中提交二维码、Base32 密钥、恢复密码或恢复码。
- 安全问题请按照 [SECURITY.md](SECURITY.md) 私下报告。

Android 签名证书见 [ANDROID-SIGNING-CERTIFICATE.md](ANDROID-SIGNING-CERTIFICATE.md)，
隐私说明见 [PRIVACY.md](PRIVACY.md)，二进制使用条款见 [LICENSE.txt](LICENSE.txt)。

> 本仓库只提供安装包、校验值和发行说明，不包含产品源代码，也不是开源源码仓库。
