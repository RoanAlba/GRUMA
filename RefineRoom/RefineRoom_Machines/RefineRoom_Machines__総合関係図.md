
# FactoryRoom × RefineRoom 総合関係図

RefineRoom は「操作卓・魂の部屋」。  
FactoryRoom は「巨大工場・身体の部屋」。  
両者は常に循環しながら作品を作り上げる。

本ファイルは両者の関係を統合した総合関係図である。

---

# 1. 全体構造（Overview）

RefineRoom（操作）  
　↓ 指示・数値・素材  
FactoryRoom（加工）  
　↓ 結果・形状・光・色・質感  
RefineRoom（表示）

この循環によって作品が成長する。

---

# 2. RefineRoom の役割（操作卓）

- 素材選択  
- 調整レバー（形・光・色・質感）  
- 図面モード  
- 保存レバー  
- 出品レバー  
- プレビュー表示  
- 呼吸アニメーション  
- 儀式具の操作  

RefineRoom は「操作」と「表示」を担う。

---

# 3. FactoryRoom の役割（工場本体）

- 成形ライン  
- 光反射ライン  
- 色処理ライン  
- 微粒子ライン  
- 仕上げライン  
- 保存処理  
- 出品処理  
- 学習システム  

FactoryRoom は「計算・加工・統合・儀式」を担う。

---

# 4. データの流れ（Data Flow）

## ● ① 素材投入
RefineRoom → FactoryRoom（成形ライン）

## ● ② 工程処理
成形 → 光反射 → 色処理 → 微粒子 → 仕上げ

## ● ③ 結果返却
FactoryRoom → RefineRoom（プレビュー更新）

## ● ④ 調整
RefineRoom のレバー操作 → FactoryRoom に再送 → 再計算

## ● ⑤ 保存
RefineRoom（保存レバー）  
→ FactoryRoom（保存処理）  
→ UI System（カード生成）

## ● ⑥ 出品
RefineRoom（出品レバー）  
→ FactoryRoom（最終儀式）  
→ 完了カード生成  
→ RefineRoom に戻る

---

# 5. 図面モードとの関係（Blueprint Link）

図面モードは FactoryRoom の内部構造を線図化して表示する。

RefineRoom（図面モード）  
　↓  
FactoryRoom（形状・寸法・内部構造データ）  
　↓  
RefineRoom（線図表示）

図面モード中は光・色・質感が弱まり、線図が優先される。

---

# 6. 学習システムとの関係（Learning Link）

RefineRoom の操作ログ  
　↓  
FactoryRoom（学習システム）  
　↓  
工程ラインの最適化  
　↓  
RefineRoom のプレビューが自然に良くなる

学習は FactoryRoom の内部で行われる。

---

# 7. 儀式具との関係（Save / Publish）

## ● 保存レバー
RefineRoom → FactoryRoom（保存処理）  
→ UI System（カード生成）  
→ RefineRoom（+2% 明るいプレビュー）

## ● 出品レバー
RefineRoom → FactoryRoom（最終儀式）  
→ 完了カード生成  
→ 画面暗転（25%）  
→ 深い呼吸（+4% → 0%）

保存＝状態の刻印  
出品＝不可逆の儀式

---

# 8. 世界観の関係（Worldview Link）

## ● RefineRoom
- 静けさ  
- 呼吸  
- 白磁・真鍮・大理石  
- 儀式具  
- 感性の部屋  

## ● FactoryRoom
- 巨大な機械  
- 真鍮・鉄・蒸気  
- 5つのラインが階層的に動く  
- 裏側の世界（音は UI に出ない）  

RefineRoom＝魂  
FactoryRoom＝身体

---

# 9. 総合関係図（Diagram）

RefineRoom（操作卓）  
- 素材選択  
- 調整レバー  
- 図面モード  
- 保存／出品  
　　　│  
　　　▼  
FactoryRoom（工場本体）  
- 成形ライン  
- 光反射ライン  
- 色処理ライン  
- 微粒子ライン  
- 仕上げライン  
- 保存処理  
- 出品処理  
　　　│  
　　　▼  
RefineRoom（結果表示）  
- プレビュー  
- 図面表示  
- 呼吸アニメーション  
- 完了カード

---

# 10. 本質（Essence）

RefineRoom は「操作と魂」。  
FactoryRoom は「実体と身体」。

両者が循環することで、  
作品は **“生まれ、育ち、完成する”**。

