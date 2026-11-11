
# Beyond These Stars · Mod 简单说明

四个独立插件，可任意装一个或多个，互不冲突。

## 一、游戏内效果

| Mod | 原版 | 安装后 |
| --- | --- | --- |
| **Peep Speed & Carry** | 村民移动速度 1.863 | ×5 → 9.314 |
| | 村民单次搬运量 1 | ×5 → 5 |
| | 住宅覆盖半径 15 格 | **50 格** |
| **Water Influence Range** | 淹水/水源地块影响距离 12 格 | **50 格**（圈内地块变湿、可耕种） |
| **Warehouse & Storage Shed Capacity** | 储物棚容量 80 | **8000** |
| | 仓库容量 360 | **36000** |
| | 容量步进（每次加量）20 | **2000** |
| | 特长「内有乾坤」加成 +20 | **+2000** |
| | 有该特长的储物棚合计 100 | **10000** |
| **Movable Forests & Instant Moves**（workbuddy 制作） | 森林被锁定，无法用「移动建筑」搬动；移动建筑要建工地、送材料、等工期 | 森林可直接搬动；移动**瞬间完成**；建筑内已存资源随建筑转移，不掉落地面 |

## 二、安装方法

1. 把下面四个 DLL 复制到游戏目录的 `BepInEx\plugins\`：

   ```
   BTS.PeepSpeedCarry.dll
   BTS.WaterInfluenceRange.dll
   BTS.StorageCapacity.dll
   BTS.MovableForests.dll
   ```

   完整路径示例：`D:\Games\Beyond These Stars\BepInEx\plugins\`

2. 启动游戏一次，插件会在 `BepInEx\config\` 下自动生成配置文件。
3. 按需改配置，**改完重启游戏**生效（Water Influence Range 例外，可热改）。

卸载：删除对应 DLL 即可（可选一并删除其 cfg）。

## 三、配置文件位置与参数

配置文件目录：`D:\Games\Beyond These Stars\BepInEx\config\`

| Mod | 配置文件 |
| --- | --- |
| Peep Speed & Carry | `marvis.bts.peepspeedcarry.cfg` |
| Water Influence Range | `marvis.bts.waterinfluencerange.cfg` |
| Warehouse & Storage Shed Capacity | `marvis.bts.storagecapacity.cfg` |
| Movable Forests & Instant Moves | `com.workbuddy.bts.movableforests.cfg` |

### Peep Speed & Carry

| 参数 | 默认 | 含义 |
| --- | --- | --- |
| `MoveSpeedMultiplier` | 5 | 村民移动速度倍率，1 = 原版 |
| `CarryMultiplier` | 5 | 单次搬运量倍率，1 = 原版（上限 255） |
| `AccommodationRange` | 50 | 住宅覆盖半径（绝对值，格）；0 或负数 = 不改 |

### Water Influence Range

| 参数 | 默认 | 含义 |
| --- | --- | --- |
| `WaterInfluenceRange` | 50 | 淹水/水源影响距离（格），原版 12，可填 1–250 |
| `PatchTerrainVisuals` | true | 是否同步地面湿痕外观；false = 只改判定不改画面 |
| `VerboseLogging` | true | 启动时是否打印每个改动项的旧值→新值 |

### Warehouse & Storage Shed Capacity

| 参数 | 默认 | 含义 |
| --- | --- | --- |
| `StorageCapacityMultiplier` | 100 | 仓库/储物棚容量倍率，1 = 原版 |
| `ScaleStorageChangeIncrement` | true | 是否同步放大容量步进（20 → 2000） |
| `ScalePerkStorageBonus` | true | 是否同步放大「内有乾坤」的 +20（→ +2000） |
| `MaxStorageCapacity` | 0 | 单建筑容量硬上限；0 = 不限制（仅受数值类型限制） |

> 卸载容量 Mod 前，请先把仓储里已分配的份额调回原版量级，否则会显示超容。

### Movable Forests & Instant Moves（workbuddy 制作，v1.2.3）

| 参数 | 默认 | 含义 |
| --- | --- | --- |
| `MovableForests` | true | 是否允许用「移动建筑」工具搬动森林；false = 恢复森林不可移动 |
| `InstantMove` | true | 是否即时完成移动（无工地、无送料、无工期）；false = 走原版移动流程 |
*（内容由AI生成，仅供参考）*
