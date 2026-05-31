# macos-11-survive
给仍然使用macos 11 的用户提供生存指南

## 日常使用
- **Clash**: Clash verge rev 2.4.4
- **Chrome**:  [Chrome 138.0.7204.184](https://www.google.com/chrome/other-platforms/)

## 开发工具

- **终端**: kitty, rio
- Github CLI: gt-2.79.0, gh-2.82.1
- **IDE**: [vs code 1.106.3(copilot 可用)](https://code.visualstudio.com/updates/v1_106), Zed
- **Coding Agent**: goose, openhands, pi, Zed

## 详细说明

### VS Code

禁用系统更新, 配置hosts
```
127.0.0.1 update.code.visualstudio.com
```

### ICU 国际化库
现在遇到 webkit, bun, 在macos 11上编译的时候使用的icu版本混乱, 直接下载的bun 1.1.20链接了系统自带的icucore 包, 缺少某些符号, 不可用.
解决问题思路:
1. 使用`sudo port install icu-devel`
2. 编译bun, webkit 时指定使用port 的 icu库: 见 [macos-11-bun-webkit](https://github.com/tq02ksu/macos-11-bun-webkit), [macos-11-bun](https://github.com/tq02ksu/macos-11-bun)
