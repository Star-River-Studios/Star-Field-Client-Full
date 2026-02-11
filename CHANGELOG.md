# 星空神域 - 客户端更新日志

## 版本号说明

本版本号专指 **「繁星计划」** 下属项目的版本标签，采用 **语义化版本（SemVer 2.0.0）** 语法，并附加项目与构建信息：
版本号结构：`MAP.MAJOR.MINOR.PATCH(-PRERELEASE)+BUILDCODE`
其中：

- **`MAP`**：地图迭代号
  - 说明：当发生**地图数据重置**时递增。每次递增后会释放若干**Beta版**，期间玩家可以提交mod列表修改申请。直到Beta版结束。一旦Beta版结束，Mod列表将固定，直到下一次版本号递增后新的Beta版。
  - 更新时间：每三年由玩家投票决定

- **`MAJOR`**：主版本号
  - 说明：当**模组加载器或游戏版本更新**时递增。
  - 更新时间：每三个月检查一次，若有更新时则进行更新。

- **`MINOR`**：次版本号
  - 说明：当**功能模块更新**时递增。
  - 更新时间：每月检查一次，若有更新时则进行更新。

- **`PATCH`**：修补版本号
  - 说明：当**配置文件更新**、**语义级紧急更新**时递增。
  - 更新时间：每15天检查一次，若有更新时则进行更新。如果存在紧急更新，则进行紧急更新。
    - 语义级紧急更新：不包括仅影响构建产物、不改变运行行为的修复。

- **`-PRERELEASE`**：预发布标识
  - 说明：当存在预发布版本时，添加该标识，并递增该标识的序号，无此后缀即为正式版。
  - 更新时间：每次地图迭代后开启，不定时更新（根据测试情况进行更新）
    - Beta：测试版，用于测试新的功能、修复bug，并提交Mod列表修改申请。
    - RC：发布候选版，用于测试Modpack的稳定性和平衡性，在此阶段中Mod列表冻结，除非遇到致命BUG（例如服务端、客户端崩溃，游戏存档死档无法再次进入等致命性BUG）否则不对Mod列表进行改动。

- **`+BUILDCODE`**：构建编号，表明该版本的构建信息。内容如下。
  - `YY`：构建年份，表明该构建是哪一年的构建
  - `M`：地图迭代次数，表明该构建属于哪一次地图重置更新（从A开始，若超过26，则进行循环，继续从A开始）
  - `NNN`：构建序号，表明该构建是第几次构建，从1开始递增，可以按构建次数补足位数
  - `P`：修补序号，表明该构建里的修补是第几次修补（从a开始，若超过26，则进行循环，继续从a开始）
    - 修补：指**构建级紧急修复**，仅影响构建产物或分发结果的修复，不引入新的功能、不改变既有语义行为。

> **版本号归零规则（SemVer 标准）**
> - 高位数字递增时，低位数字重置为0。
> - 最后一位数字`BUILD`递增时，不影响其他数字。
> - Beta阶段结束时，去掉`-PRERELEASE`后缀

## 示例
- `1.0.0.0-beta.1+26A1` 表示：
  - 地图迭代号：1
  - 主版本号：0
  - 次版本号：0
  - 修补版本号：0
  - 预发布类型：Beta 第 1 版
  - 构建号：26A1
    - 构建年份：2026
    - 地图迭代次数：A（第一次）
    - 构建序号：1（项目首次构建）
- `1.0.0.0-rc.1+26A10` 表示：
  - 地图迭代号：1
  - 主版本号：0
  - 次版本号：0
  - 修补版本号：0
  - 预发布类型：RC 第 1 版
  - 构建号：26A1
    - 构建年份：2026
    - 地图迭代次数：A（第一次）
    - 构建序号：10
- `3.2.5.8+26C325h` 表示：
  - 地图迭代号：3
  - 主版本号：2
  - 次版本号：5
  - 修补版本号：8
  - 预发布类型：正式版
  - 构建号：26C325h
    - 构建年份：2026
    - 地图迭代次数：C（第三次）
    - 构建序号：325（项目的第325次构建）
    - 修补序号：h（第8次修补）

## 更新模板
```markdown
# 星空神域 - 客户端更新（版本号：vMAP.MAJOR.MINOR.PATCH(-PRERELEASE)）

> 发布日期：YYYY-MM-DD
> ⚠️ 此为 **Beta** 测试版（或 **Release Candidate** 发布候选版），可能存在兼容性问题，欢迎反馈！（仅 Beta、RC版本添加）

## 更新介绍
（占位）

## 分发标准
- 采用 **Modrinth** 整合包格式（`.mrpack`）进行分发
- 所有资源由 **Packwiz** 统一管理
- 此为 **「繁星计划」** 下属客户端统一规范

## 变更说明

### 服务器线路变更
- **新增**
  - （占位）
- **删除**
  - （占位）
- **更新**
  - （占位）

### 技术栈变更
- **新增**
  - （占位）
- **删除**
  - （占位）
- **更新**
  - （占位）

### 模组变更
- **新增**
  - （占位）
  - **前置模组**
    - （占位）
- **删除**
  - （占位）
  - **前置模组**
    - （占位）
- **更新**
  - （占位）
  - **前置模组**
    - （占位）

### 资源变更
- **新增**
  - （占位）
- **删除**
  - （占位）
- **更新**
  - （占位）

### 配置变更
- **新增**
  - （占位）
- **删除**
  - （占位）
- **更新**
  - （占位）

## 使用指南
详细系统要求、启动器配置与安装步骤，请参阅项目 README：
- 简体中文版: [README.md](./README.md)
- 繁體中文版: [README_TW.md](./README_TW.md)
- English version: [README_EN.md](./README_EN.md)

## 加入社区
- QQ 群：[点击加入](https://qm.qq.com/q/RgessVyPC0)
- Discord：[Join Server](https://discord.gg/ekpaH4FXDF)
```

## 更新记录
# 星空神域 - 客户端更新（版本号：v1.0.0.0 Beta 1）

> 发布日期：2026-01-20
> ⚠️ 此为 **Beta** 测试版，可能存在兼容性问题，欢迎反馈！

## 更新介绍
本次更新是星空神域并入繁星计划后的首次更新，也是星空神域自2020年5月那场浩劫后的首次更新。
说实话，自从那场浩劫之后。服务器沉寂了整整六年。期间经历了项目组改组团队、改组工作室、八卦阵计划更名为繁星计划等一系列事件。
六年来，我们迫切的希望星空神域能够重现2020年刚开服时人数爆满的荣光。但如今，这个目标还很遥远。但我相信，这次更新就是迈向复兴的第一步。
我们坚信，我们终将重现当年的荣光，甚至超越当年的荣光。

## 分发标准
- 采用 **Modrinth** 整合包格式（`.mrpack`）进行分发
- 所有资源由 **Packwiz** 统一管理
- 此为 **「繁星计划」** 下属客户端统一规范

## 变更说明
本次为首次更新，没有变更说明

## 使用指南
详细系统要求、启动器配置与安装步骤，请参阅项目 README：
- 简体中文版: [README.md](./README.md)
- 繁體中文版: [README_TW.md](./README_TW.md)
- English version: [README_EN.md](./README_EN.md)

## 加入社区
- QQ 群：[点击加入](https://qm.qq.com/q/RgessVyPC0)
- Discord：[Join Server](https://discord.gg/ekpaH4FXDF)

---

# 星空神域 - 客户端更新（版本号：v1.0.0.0 Beta 2）

> 发布日期：2026-01-23
> ⚠️ 此为 **Beta** 测试版，可能存在兼容性问题，欢迎反馈！（仅 Beta 版本添加）

## 更新介绍
在本次更新中，我们添加了`Storage Drawers（储物抽屉）`、`Fluid Drawers Legacy（储液抽屉）`、`Create: Food（机械动力：食物扩展）`这三个mod。

## 分发标准
- 采用 **Modrinth** 整合包格式（`.mrpack`）进行分发
- 所有资源由 **Packwiz** 统一管理
- 此为 **「繁星计划」** 下属客户端统一规范

## 变更说明

### 模组变更
- **新增**
  - Create: Food（机械动力：食物扩展）
  - Fluid Drawers Legacy（储液抽屉）
  - Storage Drawers（储物抽屉）

## 使用指南
详细系统要求、启动器配置与安装步骤，请参阅项目 README：
- 简体中文版: [README.md](./README.md)
- 繁體中文版: [README_TW.md](./README_TW.md)
- English version: [README_EN.md](./README_EN.md)

## 加入社区
- QQ 群：[点击加入](https://qm.qq.com/q/RgessVyPC0)
- Discord：[Join Server](https://discord.gg/ekpaH4FXDF)

---

# 星空神域 - 客户端更新（版本号：v1.0.0.0 Beta 3）

> 发布日期：2026-01-27
> ⚠️ 此为 **Beta** 测试版，可能存在兼容性问题，欢迎反馈！（仅 Beta 版本添加）

## 更新介绍
在本次更新中，我们添加了`Immersive Engineering（沉浸工程）`模组及其扩展模组，并对现有模组列表进行了一次更新检查。

## 分发标准
- 采用 **Modrinth** 整合包格式（`.mrpack`）进行分发
- 所有资源由 **Packwiz** 统一管理
- 此为 **「繁星计划」** 下属客户端统一规范

## 变更说明

### 模组变更
- **新增**
  - Engineered Compatibility（兼容性扩展）
  - Engineers Delight（工程师乐事）
  - Immersive Petroleum（沉浸原油）
  - Immersive Engineering（沉浸工程）
  - Just Enough Immersive Multiblocks（JEI沉浸工程多方块结构信息）（客户端）
  - More Immersive Wires（更多沉浸线缆）
- **更新**
  - AppleSkin（苹果皮）
  - Butchery（沉浸式屠宰）
  - Create: Bits 'n' Bobs（机械动力：精致附加）
  - Create Crafts & Additions（机械动力：物品附加）
  - FerriteCore（铁氧体磁芯）
  - Integrated Dynamics（动态联合）
  - MaidUseHandCrank（女仆摇曲柄）
  - Resourcify（资源下载）（客户端）
  - Sophisticated Storage in Motion（精妙物流）
  - Sophisticated Storage（精妙存储）
  - TaCZ 1.21.1 NeoForge Port（永恒枪械工坊：零-非官方版）
  - Touhou Little Maid（车万女仆）
  - **前置模组**
    - Bagus Lib
    - Create: Dragons Plus
    - Framework
    - MaFgLib（客户端）
    - Sophisticated Core

## 使用指南
详细系统要求、启动器配置与安装步骤，请参阅项目 README：
- 简体中文版: [README.md](./README.md)
- 繁體中文版: [README_TW.md](./README_TW.md)
- English version: [README_EN.md](./README_EN.md)

## 加入社区
- QQ 群：[点击加入](https://qm.qq.com/q/RgessVyPC0)
- Discord：[Join Server](https://discord.gg/ekpaH4FXDF)

---

# 星空神域 - 客户端更新（版本号：v1.0.0.0 Release Candidate 1）

> 发布日期：2026-02-12
> ⚠️ 此为 **Release Candidate** 发布候选版，可能存在兼容性问题，欢迎反馈！

## 更新介绍
在本次版本中，我们重新添加了`Ars Nouveau（新生魔艺）`和`AnvilCraft（铁砧工艺）`模组及其附属扩展模组，并删除了一些无用或影响平衡的模组。除此之外，我们还添加了一系列扩展玩法的模组，并对现有模组进行了一次更新。
除去上述的模组改动外，我们还删除了部分纹理包，如有需要可以自行添加。

经过一段时间的测试，目前服务端、客户端均已趋于稳定。经过项目组和玩家的共同商讨后。决定结束本次Beta测试版阶段，进入RC（发布候选版）阶段。该阶段将冻结Mod列表，旨在测试mod之间的稳定性和平衡性。
针对本次Beta测试，项目组在此感谢所有参与本次测试的测试人员。
以下是本次Beta版参与测试的人员名单

> **siqixiaoye**
> **free_cat_eating**
> **Tacz_Blob**
> **yikeliulizi**
> **D4C_000**
> **CXSYGL**

感谢以上几位玩家协助项目组进行服务端、客户端的测试！

## 分发标准
- 采用 **Modrinth** 整合包格式（`.mrpack`）进行分发
- 所有资源由 **Packwiz** 统一管理
- 此为 **「繁星计划」** 下属客户端统一规范

## 变更说明

### 服务器线路变更
- **更新**
  - 所有服务端线路对应节点由`四川/成都`改为`山东/济南`

### 技术栈变更
- **更新**
  - NeoForge 模组加载器版本由`21.1.218`升级为`21.1.219`

### 模组变更
- **新增**
  - Advanced Loot Info（高级战利品信息显示）（客户端）
  - AdvancedAE（高级AE）
  - AE2 Crystal Science（应用能源：水晶科技）
  - AnvilCraft: GuideME（铁砧工艺：GuideME手册）
  - AnvilCraft（铁砧工艺）
  - AnvilCraft: PigsPlus（铁砧工艺：猪+）
  - Archaeological_Research：Exploration（考古研究：探寻）
  - Ars Additions（魔艺微调）
  - Ars Creo（机械动力扩展）
  - Ars Elemental（元素魔艺）
  - Ars Énergistique（应用能源2：新生魔艺扩展）
  - Ars Nouveau（新生魔艺）
  - Ars Technica（魔艺机械师）
  - Ars Nouveau's Flavors & Delight（魔艺乐事）
  - Better Ping Display（更好的延迟显示）（客户端）
  - Calypso's Candy Workshop（卡里普索的糖果工坊）
  - Golem Dungeons（傀儡地牢）
  - Kaleidoscope End（森罗物语：末地）
  - Kaleidoscope Nether（森罗物语：下界）
  - KubeJS（脚本引擎）
  - lpstub-all_arabic（阿拉伯数字格式包）（客户端）
  - Maid Mana Source（女仆魔源）
  - Maid Restaurant（女仆餐厅）
  - Modular Golems（傀儡装配）
  - StarbuncleMania（魔艺管道）
  - WorldEdit CUI（创世神范围显示）（客户端）
  - **前置模组**
    - L2 Library
    - Rhino
- **删除**
  - Just Enough Resources（JEI资源信息）（客户端）
  - Immersive Petroleum（沉浸原油）
  - Controlify (Controller support)（手柄支持）（客户端）
  - Chat Heads（聊天头像）（客户端）
  - Better Crafting Recipes ( whwdzg's Recipe)（更丰富的合成配方）
- **更新**
  - AE2 OMNI Cells（OMNI存储元件）
  - Applied Pneumatics（应用能源2：气动工艺扩展）
  - Create: Bits 'n' Bobs（机械动力：精致附加）
  - Create: Fast Schematic Cannon（机械动力：更快的蓝图加农炮）
  - Create: Fishery Industry（机械动力：渔业）
  - Create:Schematic Checker（机械动力：蓝图检查器）
  - Farmer's Delight（农夫乐事）
  - Fruits Delight（果园乐事）
  - Immersive Aircraft（沉浸式飞机）
  - Integrated Crafting（集成合成学）
  - Integrated Dynamics（动态联合）
  - Iris Shaders（iris着色器）（客户端）
  - Iron's Spells 'n Spellbooks（Iron的法术与魔法书）
  - Jade（玉）
  - JourneyMap（旅行地图）
  - [Let's Do] Vinery（葡园酒香）
  - Longer Chat History（更长的聊天记录）
  - More Immersive Wires（更多沉浸线缆）（修改版）
  - Neo AE2 Toogleable View Cell（AE2可切换显示元件）
  - PneumaticCraft: Repressurized（气动工艺）
  - Polymorphic Energistics（多态合成：应用能源2扩展）
  - Sophisticated Backpacks（精妙背包）
  - Sophisticated Storage（精妙存储）
  - TaCZ 1.21.1 NeoForge Port（永恒枪械工坊：零-非官方版）
  - AE Terminal View Cell Fix（显示元件槽位修复）
  - TofuCraftReload（豆腐工艺重制版）
  - TofuDelight（豆腐乐事）
  - Twilight's Flavor & Delight（暮色风味乐事）
  - **前置模组**
    - Bagus Lib
    - GTBC's SpellLib/API
    - Sophisticated Core

### 资源变更
- **新增**
  - IE: Reimmersed（资源包-模组纹理包）
- **删除**
  - Squareful（资源包-全局纹理包）
  - SummerFields（资源包-全局纹理包）
  - MultiPixel（资源包-全局纹理包）
  - Mellow（光影包）

## 使用指南
详细系统要求、启动器配置与安装步骤，请参阅项目 README：
- 简体中文版: [README.md](./README.md)
- 繁體中文版: [README_TW.md](./README_TW.md)
- English version: [README_EN.md](./README_EN.md)

## 加入社区
- QQ 群：[点击加入](https://qm.qq.com/q/RgessVyPC0)
- Discord：[Join Server](https://discord.gg/ekpaH4FXDF)