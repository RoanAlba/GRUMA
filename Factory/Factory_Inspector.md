# Factory Inspector — 詳細パネル仕様書
# （Factory_UI の右パネルに相当する領域）

## 1. Inspector の役割
Inspector は、Workspace に配置した要素（背景・装飾・図形・文字・モックアップ素材など）の  
**色・光・影・質感・サイズ・位置・効果** を調整するためのパネル。

Factory（旧RefineRoom）で制作する  
**デジタル商品の仕上げ工程** を担う。

---

## 2. Inspector の構造
Inspector は以下の 6 セクションで構成される。

1. **Color（色）**
2. **Light（光）**
3. **Shadow（影）**
4. **Transform（変形）**
5. **Effects（効果）**
6. **Meta（メタ情報）**

---

## 3. Color（色）
### ● 調整項目
- メインカラー（Primary Color）
- アクセントカラー（Accent Color）
- グラデーション（Linear / Radial）
- 透明度（Opacity）
- 色温度（Warm / Cool）

### ● 操作
- カラーピッカー
- HEX / RGB 入力
- プリセット（あなたの世界観：透明ガラス / ピンク真鍮 / 儀式光）

---

## 4. Light（光）
### ● 調整項目
- 光量（Intensity）
- 光の方向（Direction）
- 光の拡散（Spread）
- ハイライト（Highlight）
- 反射（Reflection）

### ● 世界観処理
- 光の調整は Factory 内部の “光反射ライン” が処理する
- ピンク真鍮の反射は専用アルゴリズムで再現

---

## 5. Shadow（影）
### ● 調整項目
- 影の濃さ（Strength）
- 影の距離（Distance）
- 影のぼかし（Blur）
- 影の角度（Angle）
- 内側影（Inner Shadow）

### ● 世界観処理
- 影は Factory の “質感ライン” が生成
- ガラス素材の場合は影の透明度が自動調整される

---

## 6. Transform（変形）
### ● 調整項目
- サイズ（Scale）
- 回転（Rotation）
- 位置（Position X/Y）
- 反転（Flip H / Flip V）
- レイヤー順（Z-Index）

### ● 操作
- スライダー
- 数値入力
- Workspace 上で直接ドラッグ

---

## 7. Effects（効果）
### ● 効果一覧
- グロー（Glow）
- ブラー（Blur）
- ノイズ（Noise）
- 反射（Reflection）
- 粒子（Particle）
- ガラス屈折（Glass Refraction）
- ピンク真鍮光（Brass Shine）

### ● 世界観処理
- 効果は Factory の “微粒子ライン” が処理
- ガラス系素材は屈折率を自動計算

---

## 8. Meta（メタ情報）
要素の内部情報を確認する。

- 素材ID
- カテゴリ（Background / Decoration / Shape など）
- 作成日
- 更新日
- 使用回数（Library の学習用）

---

## 9. Inspector のUIレイアウト
- 右側に縦長パネル
- セクションはアコーディオン形式で開閉
- 上から順に Color → Light → Shadow → Transform → Effects → Meta
- 選択した要素に応じて表示項目が変化

---

## 10. 備考
- Factory（旧RefineRoom）の正式仕様
- Library と Workspace と完全連動
- デジタル商品制作の “仕上げ工程” を担当
