# 朋友的酒 / FriendsWine

模组制作：**氵名音**。街霸6本地弹跳与音乐模组。

## 下载与安装

玩家请下载 Releases 附件 **FriendsWine_v0.4.4_Release.zip**；不要将 GitHub 自动生成的 Source code 当作成品安装。

安装 Fluffy Mod Manager 和支持原生插件的 REFramework，将成品 ZIP 放入管理器 `Games\SF6\Mods` 文件夹并启用，然后点击 **Launch game**。REFramework 的 `dinput8.dll` 需单独安装到游戏根目录。本项目不依赖 SF6JellyWobble、EMV Engine 或 MMDK。

## 功能

- 杰米跟随模式：一至四酒对应四档递进弹跳，双方角色一起表现；联机仅本机杰米触发。
- 常态模式：不限角色，进入对局播放音乐，支持不弹跳或四档强度。
- 四酒可旋转，三秒一圈；F11 独立开关。
- 邦多利版、思凤版手动选曲；循环补齐至弹跳周期，跨灯保留播放进度。
- 杰米二气按周期边界跳转：邦多利版 47.076923 秒，思凤版 68.769231 秒。
- 中文设置。仅本地视觉与音频，不修改攻击判定和伤害。

完整安装和控制说明见 [使用说明.txt](使用说明.txt)。

## v0.4.4 验证状态

自动回归覆盖曲线、播放进度、本机触发范围、二气临时四酒、退出停止音频，以及非杰米/旧角色缓存/控制器身份不符时拒绝跳转。最新角色限定修复的用户实机复测尚未完成。

## 构建

Windows x64，MinGW-w64 GCC/G++（支持 C++20）、Node.js、PowerShell。Lua、ImGui、JSON 和 REFramework API 依赖源码已包含。

从成品包取出 `reframework/data/FriendsWine/audio`，放到仓库根目录的 `audio` 下，再运行 `source/Build.ps1`。脚本编译插件并运行测试，产物为 `source/FriendsWine.dll`。音频测试使用所附 WAV 校验素材，真实设备测试仅输出静音。

## 致谢与许可

基于 [Overfloating0/Jamies-wine](https://github.com/Overfloating0/Jamies-wine) 修改。代码遵循 AGPL-3.0-only；第三方许可见 `licenses/`。音频不适用代码的 AGPL 授权，权利归各自权利人。
