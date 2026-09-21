# HyperVolumeANC

给澎湃 OS 4 的音量面板加一个更顺手的降噪按钮。

## 功能

- 在静音与勿扰之外新增一个音量面板实例按钮，一键切换耳机的降噪 / 通透 / 关闭
- 支持「降噪 ⇄ 通透」两态循环，也可以选「降噪 → 通透 → 关闭」三态循环
- 展开音量面板的耳机菜单可以直接断开已连接的耳机
- 切换到降噪或通透时显示超级岛提示（可在设置里关闭），切换到关闭不打扰
- 设置页可以重启作用域、查看 LSPosed 连接状态、开关降噪 / 通透通知、隐藏桌面图标、切换语言 / 主题 / 底部导航栏样式，并内置更新检查

## 支持的耳机

| 品牌 | 支持方式 |
| --- | --- |
| Xiaomi（含 Redmi） | 系统原生支持 |
| Apple 耳机 | 系统原生支持 |
| Sony / Huawei 耳机 | 需要安装对应的 SonyPods / HuaweiPods 模块 |
| OPPO 耳机 | 需要安装 OppoPods，上游 Leaf-lsgtky 版本或 1812z 分支均可，两者接口一致 |

## 使用说明

- 作用域：`com.android.systemui` 与 `com.xiaomi.bluetooth`，勾选后重启作用域
- OPPO 耳机由 OppoPods 模块接管，本模块读取它广播的降噪状态；模块没上报状态时不会显示降噪行
- 隐藏桌面图标后，可从模块管理器的「模块设置」进入本应用
- 只在小米 17 Pro Max 与红米 K90 Pro Max（小米澎湃 OS 4 Beta）上做过完整测试，其它机型可能存在差异

## 源码

https://github.com/zhhhyyyyyy/HyperVolumeANC