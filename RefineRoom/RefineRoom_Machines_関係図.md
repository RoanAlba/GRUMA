# RefineRoom × RefineRoom_Machines 関係図

RefineRoom と RefineRoom_Machines は  
「操作卓（Refine） → 内部機構（Machines） → 結果表示（Refine）」  
という循環構造で結ばれている。

RefineRoom は “操作と儀式の部屋”、  
RefineRoom_Machines は “作品の身体を生成する内部機構”。

---

## 全体構造（Overview）

┌──────────────────────────────┐
│ RefineRoom（操作卓）          │
│ UI操作 → 数値 → 指示 → Machinesへ │
└──────────────────────────────┘
                     ↓
┌──────────────────────────────┐
│ RefineRoom_Machines（内部機構） │
│ 形・光・色・質感・学習・儀式処理 │
└──────────────────────────────┘
                     ↓
┌──────────────────────────────┐
│ RefineRoom（結果表示）         │
│ プレビュー・図面・呼吸反映       │
└──────────────────────────────┘

RefineRoom → Machines → RefineRoom  
という循環で作品が実体化される。

---

## 役割の違い（Role Difference）

● RefineRoom（操作卓）
- 素材選択  
- 調整レバー  
- 図面モード  
- 保存・出品レバー  
- プレビュー表示  
- “工房の空気” を持つ  

● RefineRoom_Machines（内部機構）
- 工程ライン  
- 機械処理  
- 学習システム  
- 形・光・色・質感の生成  
- 儀式処理（保存・出品）  
- “巨大な機構の世界観” を持つ  

---

## データの流れ（Data Flow）

① 素材選択（RefineRoom）  
　↓  
② 素材ID・初期値を Machines に送る  
　↓  
③ Machines が工程ラインに流す  
　↓  
④ 各ラインの処理結果を返す  
　↓  
⑤ RefineRoom のプレビューに反映  
　↓  
⑥ レバー操作 → Machines に再送  
　↓  
⑦ Machines が再計算 → プレビュー更新  

RefineRoom は “操作”  
RefineRoom_Machines は “計算と実体化”。

---

## 儀式具との関係（Save / Publish）

● 保存レバー  
RefineRoom → Machines（保存処理） → UI System（カード生成）  
- 現在の全データを記録  
- カード生成  
- プレビューが +2% 明るくなる  

● 出品レバー  
RefineRoom → Machines（最終確定） → 完了カード  
- 全データを不可逆状態に固定  
- 出品処理  
- 完了カード生成  
- プレビューが深い呼吸  

保存＝状態の刻印  
出品＝最終儀式（不可逆）

---

## 図面モードとの関係（Blueprint Link）

図面モードは Machines の内部構造を “線図化” して表示する。

RefineRoom（図面モード）  
　↓  
RefineRoom_Machines（形状・寸法データ）  
　↓  
RefineRoom（線図として表示）

線図は Machines の “実体” を反映する。

---

## 学習システムとの関係（Learning System）

RefineRoom_Machines の学習システムは  
RefineRoom の操作ログを吸収して賢くなる。

RefineRoom（操作）  
　↓  
Machines（ログ蓄積）  
　↓  
学習システム（傾向分析）  
　↓  
Machines（工程の最適化）  
　↓  
RefineRoom（自然に良く見えるプレビュー）

RefineRoom は “操作”  
Machines は “学習と最適化”。

---

## 世界観の関係（Worldview Link）

● RefineRoom  
- 静けさ  
- 呼吸  
- 白磁・真鍮・大理石  
- 儀式具  
- 感性の部屋  

● RefineRoom_Machines  
- 巨大な機構  
- ライン  
- 真鍮・鉄・蒸気  
- 工程の動き（UIには音を出さない）  
- 実体の部屋  

RefineRoom＝魂  
RefineRoom_Machines＝身体

---

## 関係図（Diagram）

┌──────────────────────────────┐
│ RefineRoom（操作卓）          │
│ ・素材選択                     │
│ ・調整レバー                   │
│ ・図面モード                   │
│ ・保存／出品レバー             │
└───────────────┬───────────────┘
                    │ 指示・数値・素材
                    ▼
┌──────────────────────────────┐
│ RefineRoom_Machines（内部機構） │
│ ・工程ライン                     │
│ ・機械処理                       │
│ ・学習システム                   │
│ ・儀式処理                       │
└───────────────┬───────────────┘
                    │ 結果・形状・質感
                    ▼
┌──────────────────────────────┐
│ RefineRoom（結果表示）         │
│ ・プレビュー                     │
│ ・図面表示                       │
│ ・呼吸アニメーション             │
└──────────────────────────────┘

---

## ✔ 最短まとめ

- RefineRoom＝操作卓  
- RefineRoom_Machines＝内部機構  
- RefineRoom → Machines → RefineRoom の循環構造  
- 保存・出品は Machines
