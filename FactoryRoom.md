
# FactoryRoom

GRUMA の「工場本体」。  
売れる確率アルゴリズムと学習システムを内部で処理する中枢。

---

## 1. FactoryRoom の役割
- 工程の進行（形・光・色・質感・仕上げ）
- 売れる確率の計算（ProbabilityCore）
- 作者の操作の学習（LearningCore）
- 工程の監視と同期（ProcessSync）
- RefineRoom への確率出力

---

## 2. 売れる確率アルゴリズム
（ここに貼る：重み付け・計算式・工程別ブースト）

---

## 3. 学習システム（Learning System）
（ここに貼る：選択学習・行動学習・結果学習）

---

## 4. FactoryRoom 接続仕様（Core Integration）
（ここに貼る：ProbabilityCore / LearningCore / ProcessSync の説明）

---

## 5. FactoryRoom 内部構造図
（ここに貼る：内部構造図の統合版ブロック）

---

## 6. データの流れ
（ここに貼る：ProcessSync → ProbabilityCore → RefineRoom の図）

---

## 7. 工程順での動作
（ここに貼る：素材 → 形 → 光 → 色 → 質感 → 仕上げ → Undo）

---

## 8. 目的
- FactoryRoom を “売れる確率を計算する工場” にする
- FactoryRoom を “使うほど賢くなる工場” にする
- RefineRoom は UI として軽く保つ
- 工程の動きと確率計算を完全同期させる
- Undo を自然に巻き戻す
