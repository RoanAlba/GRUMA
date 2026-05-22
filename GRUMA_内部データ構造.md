# GRUMA_内部データ構造（完全統合版）

本仕様書は、GRUMA 全体の内部データ構造（Data Structure）と  
図面モード（Blueprint Mode）の仕様を  
“世界観を壊さない技術層” として統合して定義する。

GRUMA のデータは、作品の旅路に沿って階層的に整理される。

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

# 10. 図面モード（Blueprint Mode）

図面モードは、GRUMA 全体の構造を “線図（Blueprint）” として表示する  
技術視点モードである。

世界観の光・影・素材を薄くし、  
構造・動線・境界だけを静かに浮かび上がらせる。

---

# 11. 図面モード UI 配置

## 11-1. 図面モードの起動 UI（右上トグル）
- 画面右上に白金の小さなトグルボタン  
- 通常時は 20% の透明度  
- ホバー／タップでふわっと 100%  
- ON：0.2 秒で線図化  
- OFF：元の世界観に戻る  

---

## 11-2. 図面モード中の UI 最小構成

・全体俯瞰ビュー（中央）  
・部屋境界ライン（点線）  
・部屋名ラベル（細いサンセリフ）  
・拡大縮小 UI（右側）  
・部屋詳細ボタン（各部屋の中央下）  

---

## 11-3. 全体俯瞰ビュー（中央）

FactoryRoom → RefineRoom → ExhibitionRoom → ListingRoom → OuterWorld  
の順で横一列に線図表示。

- 線色：#1a1a1a  
- 背景：工房の空気色を 70% 薄く  
- 影・質感・光：すべてオフ  
- 呼吸アニメ：1/4 の弱さ  

---

## 11-4. 部屋境界ライン（点線）

点線色：#2a2a2a  
境界の意味も薄く表示：

Factory ↔ Refine：戻れる  
Refine → Exhibition：戻れない  
Exhibition → Listing：儀式前  
Listing → OuterWorld：完全に戻れない  

---

## 11-5. 拡大縮小 UI（右側）

- 縦スライダー  
- 触るまで 20% 透明  
- 拡大率：0.5x ～ 3x  
- 線の太さは一定  

---

## 11-6. 部屋詳細ボタン（中央下）

白金の小さな丸ボタン  
タップで “部屋の図面詳細” へ。

詳細ビューでは：

・Machines の位置  
・UI の配置  
・動線  
・同期ライン  
・部屋固有の構造  

戻るボタンは左上に小さく配置。

---

## 11-7. 図面モード中に非表示になるもの

・光の演出  
・素材の質感（白磁・真鍮・ガラス）  
・影  
・動画モックアップ  
・展示演出  
・出品ゲートの光  
・通常 UI（レバー・棚・ボタン）  

---

# 12. 図面モードの目的（再掲）

- GRUMA 全体の構造を俯瞰  
- 動線・境界・配置の破綻を早期発見  
- 世界観を薄くして構造だけを見る  
- 技術層の確認を世界観を壊さずに行う  

