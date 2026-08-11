# ChronaKey Releases

ChronaKey 的官方二进制发行仓库。ChronaKey 是本地离线运行的多平台双因素验证器；
账户密钥、二维码和备份内容由客户端在本机处理。

> 本仓库只提供安装包、校验值和发行说明，不包含产品源代码，也不是开源源码仓库。
> ChronaKey 当前仍处于 Alpha 测试阶段，请只使用测试账户，妥善保留原验证器和恢复码。

## 下载

请只从 [GitHub Releases](https://github.com/rw0104/ChronaKey-Releases/releases) 下载，
并核对每个版本附带的 `SHA256SUMS`：

```powershell
Get-FileHash .\ChronaKey-Windows-x64-unsigned-setup.exe -Algorithm SHA256
```

```bash
sha256sum -c SHA256SUMS
```

## 当前交付通道

| 平台 | 测试包 | 当前限制 |
| --- | --- | --- |
| Android | Release APK | 使用 ChronaKey 长期 Release 证书签名；指纹见 `ANDROID-SIGNING-CERTIFICATE.md` |
| Windows | x64 NSIS 安装程序 | 尚未进行 Authenticode 签名，可能触发 SmartScreen |
| Linux | `.deb`、`.AppImage` | runner 恢复后提供 |
| macOS | Universal `.dmg` | 后续提供；未公证测试包会触发 Gatekeeper |
| iOS | TestFlight 或受控真机包 | 需要 Apple 签名，不通过公共 Release 分发 Ad Hoc IPA |

## 安全原则

- 安装前核对文件名、版本和 SHA-256。
- Alpha 阶段不要迁移唯一一份生产 2FA 密钥。
- 不要在 Issue、截图或日志中提交二维码、Base32 密钥、恢复密码或恢复码。
- 安全问题请按照 [SECURITY.md](SECURITY.md) 私下报告。

Android 签名证书见 [ANDROID-SIGNING-CERTIFICATE.md](ANDROID-SIGNING-CERTIFICATE.md)，
隐私说明见 [PRIVACY.md](PRIVACY.md)，二进制使用条款见 [LICENSE.txt](LICENSE.txt)。
