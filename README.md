# 霓虹壁球 SquashNeon

一个霓虹风格的壁球小游戏：控制球拍接球，连击涨分，10 关通关制，有奖章系统、云端排行榜、中英双语。单文件 HTML 实现，无广告、无内购、完全免费。

## 怎么玩

- 移动鼠标 / 手指滑动控制球拍，点击发球
- 每 8 次接球进入下一关，共 10 关
- 连击（Combo）和完美接球（Perfect）会大幅加分

## 下载 / 在线玩

| 版本 | 入口 | 说明 |
|---|---|---|
| 网页版 | [点这里直接玩](https://squash-neon.app.workbuddy.host/?sharecode=65N5MVPOMU) | 无需安装，手机电脑都行 |
| 安卓版 | [下载 APK](../../releases/latest/download/SquashNeon.apk) | 90 KB，Android 7.0+，横屏 |
| Windows 版 | [下载 EXE](../../releases/latest/download/SquashNeon.exe) | 228 KB，Win10/11，免安装 |

安卓安装时系统会提示「未知来源应用」，允许即可（个人发布 App 的正常提示）。
Windows 下载后直接双击运行；若提示「未知的发布者」，选择「仍要运行」。

## 技术说明

- 纯单文件 HTML5 Canvas，无第三方游戏引擎
- 云端排行榜基于 PostgREST 语义的数据库调用，已收敛为 cloudApi 适配层（8 个原子操作），方便迁移后端
- 安卓版：Java 壳（内嵌固定端口本地 HTTP 服务 + WebView），手工最小构建链（aapt2 / d8 / zipalign / apksigner）
- Windows 版：pywebview + WebView2 壳，PyInstaller 打包
- 桌面与安卓壳本地存储端口固定，保证 localStorage 身份持久

## 版本

- **V 3.6.2**（2026-11-06）：云调用收敛为 cloudApi 适配层；SDK 版本钉死；离线体验文案修正
- **V 3.6**：中英双语
- **V 3.5**：身份绑定设备，改名不分裂
- **V 3.4**：新用户免输入自动分配名字
- 更早版本见游戏内更新提示

## 许可

个人作品，仅供娱乐。代码可供学习参考，请勿用于商业用途。
