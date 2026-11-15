---
AIGC:
    Label: "1"
    ContentProducer: 001191440300708461136T1XGW3
    ProduceID: 7132863172ab089064a045917be9e18a_ffa794b0e12111f18c5752540024e231
    ReservedCode1: Y7Z8Bu6xvshGCbGUVRDjITbr4qC16mcICVYJ1nN3hItMx8qBUlEBReGQndMauSO4MIubzjyfAzzDCQOMAbG3bUYuN8y7qyE1TycxaK2UtTpeHnI8w5BNPW8/+gWpEYlQBjiclgREMDcZnaBO6VeV6XSLnaHJkMDQ6D4WVutOBgGDsWfvkikp8x+wD/M=
    ContentPropagator: 001191440300708461136T1XGW3
    PropagateID: 7132863172ab089064a045917be9e18a_ffa794b0e12111f18c5752540024e231
    ReservedCode2: Y7Z8Bu6xvshGCbGUVRDjITbr4qC16mcICVYJ1nN3hItMx8qBUlEBReGQndMauSO4MIubzjyfAzzDCQOMAbG3bUYuN8y7qyE1TycxaK2UtTpeHnI8w5BNPW8/+gWpEYlQBjiclgREMDcZnaBO6VeV6XSLnaHJkMDQ6D4WVutOBgGDsWfvkikp8x+wD/M=
---

# Beyond These Stars — 自用 Mod 合集

6 个相互独立的 BepInEx 5 Mod，可任意安装其中几个，互不依赖。

| Mod | 版本 | 一句话效果 |
|-----|------|-----------|
| Movable Forests & Instant Moves | 1.2.5 | 森林可移动；移动/建造立即完成；资源随建筑一起搬 |
| Landscaper Work Range | 1.4.2 | 造景师作业范围 50 格；造景工地建造时间 1/10；挖填不再破坏土壤肥力 |
| Peep Speed & Work Range | 1.9.0 | 村民移速 5 倍；住宅招工范围 50 格 |
| Warehouse & Storage Shed Capacity | 1.2.0 | 大仓库/小仓库容量 100 倍 |
| Spaceport & Trade Spaceship Storage | 1.0.1 | 太空港容量 10000；贸易飞船容量 400 |
| Water Influence Range | 1.0.0 | 水源湿润/肥沃影响范围 12 → 50 格 |

安装：把需要的 `.dll` 放进游戏目录 `BepInEx/plugins/`，启动游戏后自动在 `BepInEx/config/` 生成各自的 cfg。

---

## Movable Forests & Instant Moves

森林不再被锁定，可用「移动建筑」工具搬动；移动建筑或森林时跳过工地、材料运输和建造时间；建筑内已存的资源原样搬进新位置，不掉成地面资源堆；移动后库存上限与重载存档一致，不会随移动次数虚增。

配置文件：`BepInEx/config/com.workbuddy.bts.movableforests.cfg`

| 参数 | 默认 | 含义 |
|------|------|------|
| `MovableForests` | `true` | 是否允许移动森林；`false` 恢复原版不可移动 |
| `InstantMove` | `true` | 是否即时完成移动；`false` 走原版建工地流程 |

## Landscaper Work Range

造景师（Landscaper）的作业半径改为 50 格（原版较小）；该 Mod 附带的三个造景工地（地形改造、堆肥、植树）建造时间缩到 1/10；地形改造（挖低/填高）完成后不再把土壤退化为裸地，肥力保留，同时堵掉采集、建筑溢出、新矿脉暴露等其他会把沃土变裸地的路径。

配置文件：`BepInEx/config/marvis.bts.landscaperworkrange.cfg`

| 参数 | 默认 | 含义 |
|------|------|------|
| `LandscaperWorkRange` | `50` | 造景类建筑的作业半径（格），直接替换原版值；≤0 保持原版 |
| `IncludeAllLandscapingBuildings` | `false` | 是否同样作用于其他造景建筑（原版 Reformer，36 格） |
| `WorkSiteTimeScale` | `0.1` | 三个造景工地的建造时间倍率，1 = 原版，≤0 关闭 |
| `ScaleWorkSiteDeliveryTime` | `true` | 是否同时缩放单次送料时间（堆肥工地原版 20 秒） |
| `PreserveTileTypeOnTerraform` | `true` | 挖填完成后保留土壤类型（肥力不丢） |
| `PreserveTileTypeOnResourceRemoval` | `true` | 采集/移除资源时不把沃土退化为裸地 |
| `PreserveTileTypeOnResourceDeposit` | `true` | 挖出新矿脉时脚下保留沃土 |

## Peep Speed & Work Range

村民移动速度提升到 5 倍，赶路和送货明显变快；住宅的招工半径改为 50 格，村民可在更大范围内选择工作。

配置文件：`BepInEx/config/marvis.bts.peepspeedcarry.cfg`

| 参数 | 默认 | 含义 |
|------|------|------|
| `MoveSpeedMultiplier` | `5` | 村民移动速度倍率，1 = 原版 |
| `AccommodationRange` | `50` | 住宅招工半径（格），直接替换原版值；≤0 保持原版 |

## Warehouse & Storage Shed Capacity

大仓库与小仓库的存储容量放大 100 倍（大仓库 360 → 36000，小仓库 80 → 8000）；库存滑条步长同步放大，避免手动拉条太慢；「Bigger On The Inside」perk 的 +20 也按同倍率放大。

配置文件：`BepInEx/config/marvis.bts.storagecapacity.cfg`

| 参数 | 默认 | 含义 |
|------|------|------|
| `StorageCapacityMultiplier` | `100` | 仓库容量倍率，1 = 原版 |
| `ScaleStorageChangeIncrement` | `true` | 是否同步放大滑条步长 |
| `StorageChangeIncrement` | `1000` | 滑条步长绝对值；`0` = 按倍率缩放原版 20 |
| `MaxStorageCapacity` | `0` | 单建筑容量上限，`0` = 不额外限制 |
| `ScalePerkStorageBonus` | `true` | 是否把 perk 的 +20 一起按倍率放大 |

## Spaceport & Trade Spaceship Storage

太空港（含已落地的定居飞船）总容量 720 → 10000，滑条步长 20 → 200；贸易飞船容量 80 → 400，相关 perk 加成的数值同步放大。

配置文件：`BepInEx/config/marvis.bts.spaceporttradestorage.cfg`

| 参数 | 默认 | 含义 |
|------|------|------|
| `Spaceport.Capacity` | `10000` | 太空港/定居飞船总容量（原版 720） |
| `Spaceport.ChangeIncrement` | `200` | 太空港滑条步长（原版 20） |
| `TradeSpaceship.Capacity` | `400` | 贸易飞船容量（原版 80） |
| `TradeSpaceship.ExtraSpacePerkBonus` | `100` | 飞船扩容 perk 的固定加成（原版 20），`0` = 忽略 |
| `TradeSpaceship.UbloMultiplierPercent` | `150` | 飞船扩容 perk 的百分比倍率（原版 150），`100` = 关闭 |

## Water Influence Range

判定「土壤是否被水源滋润」的距离从 12 格放宽到 50 格，离水更远的土地也能变湿、可变肥沃；湿润地表的视觉边界同步扩大，与判定一致。

配置文件：`BepInEx/config/marvis.bts.waterinfluencerange.cfg`

| 参数 | 默认 | 含义 |
|------|------|------|
| `WaterInfluenceRange` | `50` | 水源影响半径（格，1–250），原版 12 |
| `PatchTerrainVisuals` | `true` | 是否同步湿润地表的视觉边界 |
| `VerboseLogging` | `true` | 启动时记录每个被修改方法的旧值/新值 |

---

所有 Mod 只改客户端数值与逻辑，不改存档结构；参数修改后重进游戏生效。
*（内容由AI生成，仅供参考）*
