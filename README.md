# 法杖盾斧

《怪物猎人 荒野》充能斧外观替换：日式魔女法杖 + 时钟法阵。

替换武器：**白炽斧耶利米 / 炽光斧耶利米**

![](previews/axe.jpg)

实机：

| 剑盾形态 · 防御中 | 站立 |
|---|---|
| ![](previews/shield.jpg) | ![](previews/stance.jpg) |

## 下载

[RuneStaff-v1.2.zip](RuneStaff-v1.2.zip)

## 更新（v1.2）

- **法阵改成双态**：剑盾形态举盾防御时浮现完整的星钟法阵；切到斧形态，法阵内面变成两把新月刃，共用外圈与罗马数字环。两态靠读取武器形态切换，不延迟、不需要额外动作。
- **蓝膜光感**：盾面与月牙各自一套 2048×512 图集，中心降低饱和度、向边缘过渡到冷蓝；粗糙度从中心约 0.48 过渡到边缘约 0.32，法线只加低幅缓曲率。
- **蓝色轴心**换成独立的抛光宝石材质。
- **杖头与颈部**局部曲面精修。

## 前置

- REFramework。没有它 `pak_mods` 不加载，mod 无效。
- REFramework → Advanced Options → 打开 **Alternate PAK Folder**。

## 安装

把 `RuneStaff-v1.2.zip` 拖进 Fluffy Mod Manager，启用。

装过 v1.0 / v1.1 的直接覆盖，**它带的新显隐脚本会替换掉旧的**。

## 效果

- 剑盾形态按住 R 防御：星钟法阵出现
- 剑盾形态平时：法阵隐藏
- 斧形态：双月刃常显

## 卸载

Fluffy 里取消勾选或删除。

## 排错

| 症状 | 处理 |
|---|---|
| 没有任何变化 | 检查 REFramework 和 Alternate PAK Folder |
| 杖身是默认材质 | 贴图没读到，反馈一下 |
| 防御时法阵不出 | 确认 `<游戏目录>\reframework\autorun\rune_guard_circle.lua` 在。日志：`<游戏目录>\reframework\data\rune_guard_circle.log` |
| 法阵闪烁 | 装过 ArmorVariantManager 且配过这把武器的显隐。删掉 `reframework\data\ArmorVariantManager\it0900_0021.json` |

不需要"防御时才显示"的话，删掉 `rune_guard_circle.lua`，法阵就常显。

## 附注

截图中的角色皮肤是 mod「理科魔女 / Witch Shinano」，作者 Fruit milk。

- 主页：[space.bilibili.com/2438342](https://space.bilibili.com/2438342)
- 本 mod 不分发它，也不依赖它。法杖配饰的造型参考了那个角色的设计。

几何经由 Tripo AI 重拓扑回传，再在 Blender 里做保形精修、双态拆分与材质调整；打包用 [ree-pak-cli](https://github.com/NSACloud/ree-pak-cli)，网格导入导出用 RE-Mesh-Editor。

## 许可

与 Capcom 无关联。《怪物猎人 荒野》及其资产版权归 Capcom。

`RuneStaff.pak` 是游戏原有资源的修改产物，请在自己拥有该游戏的机器上使用。

内置的 `rune_guard_circle.lua` 为本项目原创，MIT。
