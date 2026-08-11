# Android Signing Certificate

ChronaKey Android APK ??? Release ?????

| ?? | ? |
| --- | --- |
| Android application ID | `com.chronakey.authenticator` |
| Subject | `CN=ChronaKey Android Release, O=ChronaKey` |
| Key | RSA 4096-bit |
| Certificate SHA-256 | `638d5a56b337613637e475d830440f81250c049dc3af091be0206c64b6dc62fd` |
| ???? | `v0.1.0-alpha.1` |

?? APK ???? Android SDK `apksigner` ???

```bash
apksigner verify --verbose --print-certs ChronaKey-Android-release.apk
```

???? `Signer #1 certificate SHA-256 digest` ??????????????????
??????? Private Vulnerability Reporting ??????
