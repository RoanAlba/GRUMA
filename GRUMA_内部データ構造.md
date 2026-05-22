# GRUMA_内部データ構造（正式版）

本仕様書は、GRUMA 全体の内部データ構造（Data Structure）を  
“世界観を壊さない技術層” として定義する。

GRUMA のデータは、作品の旅路に沿って  
階層的に整理される。

---

# 1. 最上位構造（Top Level）

GRUMA
├─ Rooms（部屋）
├─ Works（作品）
├─ Machines（同期・処理）
├─ Mockups（モックアップ）
├─ Market（外界ステータス）
└─ System（内部設定）


---

# 2. Rooms（部屋構造）

Rooms
├─ FactoryRoom
├─ RefineRoom
├─ ExhibitionRoom
├─ ListingRoom（出品部屋）
└─ OuterWorld（外界）


各部屋は “役割” と “境界” を持つ。

- FactoryRoom：制作  
- RefineRoom：整える  
- ExhibitionRoom：展示  
- ListingRoom：出品  
- OuterWorld：出品後の管理  

---

# 3. Works（作品データ）

Works
├─ WorkID
├─ Metadata
│    ├─ Title
│    ├─ Category
│    ├─ CreatedAt
│    ├─ Tags
│    └─ Palette
├─ State（状態）
│    ├─ Creating
│    ├─ Refining
│    ├─ Completed
│    ├─ Exhibiting
│    ├─ Listing
│    └─ OuterWorld
├─ Assets（素材）
│    ├─ BaseImage
│    ├─ Layers
│    ├─ MockupImages
│    └─ VideoMockups
└─ MarketInfo（外界情報）
├─ ListingID
├─ Status（Listed / Sold / Paused / Closed）
├─ MarketName
└─ ListedAt


---

# 4. Machines（同期・処理）

Machines
├─ LightSync
├─ ShadowSync
├─ TextureSync
├─ MotionSync
└─ Exporter


### Machines の役割
- 光・影・質感・動きを作品に同期  
- モックアップとの整合性を保つ  
- 書き出し処理を担当  

---

# 5. Mockups（モックアップ）

Mockups
├─ StaticMockups（静止）
│    ├─ Category
│    ├─ Preview
│    └─ Rules
└─ VideoMockups（動画）
├─ Category
├─ Preview
└─ SyncRules


### SyncRules
- 光追従  
- 影追従  
- パース補正  
- 動きの遅延  

---

# 6. Market（外界ステータス）

Market
├─ ListingID
├─ Status（Listed / Sold / Paused / Closed）
├─ MarketName
├─ Price
├─ ListedAt
└─ History（外界での履歴）


GRUMA 内では **閲覧のみ**。

---

# 7. System（内部設定）

System
├─ BlueprintMode（図面モード）
│    ├─ LineColor
│    ├─ BackgroundFade
│    ├─ AnimationLevel
│    └─ HiddenElements
├─ UIConfig
└─ RoomTransitions


---

# 8. 作品の状態遷移（State Machine）

Creating → Refining → Completed → Exhibiting → Listing → OuterWorld


戻れるのは **Creating ↔ Refining** のみ。  
Completed 以降は戻らない（コピーのみ可能）。

---

# 9. データの流れ（Data Flow）

FactoryRoom → RefineRoom → ExhibitionRoom → ListingRoom → OuterWorld


各部屋は “データの受け渡し” のみ行い、  
編集権限は部屋ごとに固定される。

---

# 10. まとめ（核心）

- GRUMA のデータは **作品の旅路に沿って階層化**  
- Rooms / Works / Machines / Mockups / Market / System の6構造  
- 作品は State Machine に沿って進む  
- Completed 以降は戻らない（世界観の一貫性）  
- 図面モードは System 層に属する技術視点  

