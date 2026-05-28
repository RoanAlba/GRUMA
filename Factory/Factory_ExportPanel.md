# Factory Export Panel — 書き出しパネル仕様書
# （Factory_UI の下部に配置される領域）

## 1. Export Panel の役割
Export Panel は、Factory（旧RefineRoom）で制作した  
**デジタル商品を最終的な形式で書き出すためのパネル**。

テンプレート、モックアップ、背景、UIパーツ、動画など  
すべての “完成品” がここから生成される。

---

## 2. Export Panel の構造
Export Panel は以下の 3 セクションで構成される。

1. **Format（書き出し形式）**
2. **Settings（設定）**
3. **Generate（生成ボタン）**

---

## 3. Format（書き出し形式）
### ● 静止画（Image）
- PNG  
- JPG  
- WebP  
- 背景透過（ON/OFF）

### ● PDF
- A4 / US Letter / カスタムサイズ  
- 余白設定（0〜40px）

### ● 動画（必要な場合）
- MP4  
- MOV  
- ループ（ON/OFF）  
- 解像度（1080p / 4K）

### ● その他（Factory 拡張）
- SVG（図形ベースのテンプレート用）
- JSON（UIパーツのデータ書き出し）

---

## 4. Settings（設定）
### ● 解像度プリセット
- 1:1（正方形）
- 4:5（Instagram）
- 16:9（横長）
- 9:16（縦長）
- カスタムサイズ（px 指定）

### ● 品質設定
- 低 / 中 / 高 / 最高  
（Factory 内部の “圧縮炉” が最適化を担当）

### ● カラープロファイル
- sRGB  
- Display P3  
- CMYK（PDF のみ）

### ● メタデータ
- タイトル  
- 作者（自動で “やっちゃん”）  
- 作成日（自動）  
- タグ（Library と連動）

---

## 5. Generate（生成ボタン）
### ● ボタン動作
- 「Generate」ボタンを押すと、Factory の奥にある  
　**“圧縮炉（Compressor Furnace）”** が稼働する。
- 光が走り、内部の機構が静かに動き、  
　最適化されたデジタル商品が生成される。

### ● 生成後の動作
- プレビュー表示  
- 保存先を選択  
- “展示室（Gallery）へ送る” ボタン  
- “再編集に戻る” ボタン

---

## 6. Export Panel のUIレイアウト
- 下部に横長パネルとして固定表示
- 左：Format  
- 中央：Settings  
- 右：Generate ボタン  
- 生成中はピンク真鍮の光がアニメーションする

---

## 7. 世界観（GRUMA仕様）
- Export は工房の “最終儀式” に相当する
- 圧縮炉が光り、透明ガラスの管を通ってデータが流れる
- ピンク真鍮の縁取りが完成品の種類に応じて色を変える
- 完成品は “光の粒” として現れ、ファイルとして保存される

---

## 8. 備考
- Factory（旧RefineRoom）の正式書き出し仕様
- Library / Workspace / Inspector と完全連動
- デジタル商品制作の “最終工程” を担当
