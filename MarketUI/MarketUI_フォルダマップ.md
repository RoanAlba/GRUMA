# MarketUI — フォルダマップ（正式版）

MarketUI 全体のフォルダ構造をまとめたマップ。  
一覧・詳細・計器ページの三本柱と、  
MarketFit 計器を含む計器ページ専用フォルダを明確に分離する。

---

# ■ MarketUI フォルダ構造（全体）

MarketUI/
├─ MarketUI_総合仕様.md
├─ MarketUI_UI構造図.md
├─ MarketUI_UI遷移図.md
├─ MarketUI_工程まとめ.md
├─ MarketUI_フォルダマップ.md   ← このファイル
└─ 計器ページ/
      ├─ GRUMA_計器_基準仕様.md
      ├─ GRUMA_計器_基準仕様_完全版.md
      └─ MarketFit_計器_完成仕様.md

---

# ■ フォルダの役割

### ● MarketUI/（直下）
- MarketUI 全体の上位仕様  
- UI構造・遷移・工程・フォルダマップ  
- MarketUI の“骨格”を定義するファイル群  
- ページ単位の仕様はここに置く

### ● MarketUI/計器ページ/
- 計器ページ（分析UI）専用フォルダ  
- MarketFit 計器を含む全計器の仕様  
- 基準仕様・完全版・個別仕様をまとめる  
- MarketUI の中でも“分析UI”だけを担当

---

# ■ ファイルの役割一覧

### ● MarketUI_総合仕様.md
MarketUI の世界観・目的・禁止事項を定義する親ファイル。

### ● MarketUI_UI構造図.md
一覧・詳細・計器ページの UI の骨格を定義。

### ● MarketUI_UI遷移図.md
ページ間の動線（一覧 → 詳細 → 計器）を固定。

### ● MarketUI_工程まとめ.md
MarketUI を作る順番・工程・確認項目をまとめる。

### ● MarketUI_フォルダマップ.md
MarketUI 全体のフォルダ構造を固定する（このファイル）。

### ● 計器ページ/ 以下
- GRUMA_計器_基準仕様.md  
- GRUMA_計器_基準仕様_完全版.md  
- MarketFit_計器_完成仕様.md  

計器ページの UI・世界観・個別仕様をまとめる。

---

# ■ このファイルの役割

- MarketUI 全体のフォルダ構造を固定  
- 上位仕様と計器ページ仕様を明確に分離  
- 迷子ゼロの構造を保証  
- MarketUI の“地図”として機能する
