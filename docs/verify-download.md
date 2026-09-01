# 校验官方下载

> 当前没有公开安装包。本页中的文件名和校验值将在正式 Release 时填写。

## 1. 确认来源

只从 README 列出的官方网站或本仓库 Releases 页面下载。不要使用搜索广告、群聊附件、网盘转存或来源不明的镜像。

## 2. 核对 SHA-256

正式 Release 会同时列出文件名和 SHA-256。下载后在“终端”中运行：

```bash
shasum -a 256 "/path/to/Pointrans-X.Y.Z.dmg"
```

输出必须与对应 Release 中的值逐字一致。不要使用其他版本页面的校验值。

## 3. 检查签名和苹果公证

把应用拖入“应用程序”后，可以运行：

```bash
codesign --verify --deep --strict --verbose=2 "/Applications/Pointrans.app"
spctl --assess --type execute --verbose=2 "/Applications/Pointrans.app"
```

正式版本应通过签名和 Gatekeeper 验证。若验证失败，请停止使用并通过官方支持入口报告，不要尝试移除 quarantine、关闭 Gatekeeper 或降低系统安全设置。

## 4. 校验值不一致

- 删除下载文件；
- 不要打开或转发；
- 记录下载页面、文件名、时间和实际 SHA-256；
- 通过 Download Help 或私密安全入口报告。

