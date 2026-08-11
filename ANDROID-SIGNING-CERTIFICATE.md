# Android Signing Certificate

ChronaKey Android APK 的长期 Release 签名身份：

| 字段 | 值 |
| --- | --- |
| Android application ID | `com.chronakey.authenticator` |
| Subject | `CN=ChronaKey Android Release, O=ChronaKey` |
| Key | RSA 4096-bit |
| Certificate SHA-256 | `638d5a56b337613637e475d830440f81250c049dc3af091be0206c64b6dc62fd` |
| 首次使用 | `v0.1.0-alpha.1` |

下载 APK 后可使用 Android SDK `apksigner` 核对：

```bash
apksigner verify --verbose --print-certs ChronaKey-Android-release.apk
```

输出中的 `Signer #1 certificate SHA-256 digest` 必须与上表完全一致。出现其他指纹时，
不要安装并通过 Private Vulnerability Reporting 联系维护者。
