# RefineRoom × FactoryRoom 関係図
RefineRoom と FactoryRoom は
「操作卓（Refine） → 工場本体（Factory）」  
という構造で結ばれている。

RefineRoom は 工場を操作する UI、
FactoryRoom は 実際に素材が加工される場所。

1. 全体構造（Overview）

┌──────────────────────────────┐
│         RefineRoom（操作卓）         │
│  UI操作 → 数値 → 指示 → FactoryRoomへ │
└──────────────────────────────┘
                     ↓
┌──────────────────────────────┐
│        FactoryRoom（工場本体）        │
│   工程・ライン・機械・学習・確率処理   │
└──────────────────────────────┘
                     ↓
┌──────────────────────────────┐
│         RefineRoom（結果表示）        │
│     プレビュー・図面・呼吸・質感反映     │
└──────────────────────────────┘

RefineRoom → FactoryRoom → RefineRoom  
という循環構造になっている。

2. 役割の違い（Role Difference）
● RefineRoom（操作卓）
UI操作の中心

素材選択

調整レバー

図面モード

保存・出品レバー

プレビュー表示

“工房の空気” を持つ

● FactoryRoom（工場本体）
工程ライン

機械の動作

素材の加工

確率アルゴリズム

学習システム

出力データ生成

“巨大な機械の世界観” を持つ

3. データの流れ（Data Flow）

① 素材選択（RefineRoom）
　↓
② 素材ID・初期値を FactoryRoom に送る
　↓
③ FactoryRoom が素材を工程に流す
　↓
④ 工程ごとの処理結果を返す
　↓
⑤ RefineRoom のプレビューに反映
　↓
⑥ 調整レバー操作 → FactoryRoom に再送
　↓
⑦ FactoryRoom が再計算 → プレビュー更新

RefineRoom は“操作”
FactoryRoom は“計算と実体”  
という役割分担。

4. 儀式具との関係（Save / Publish）
● 保存レバー

RefineRoom → FactoryRoom（状態保存） → UI System（カード生成）

FactoryRoom が「保存時点の工程データ」を記録

UI System にカードとして追加

RefineRoom に戻る

● 出品レバー

RefineRoom → FactoryRoom（最終確定） → 出品処理 → 完了カード

FactoryRoom が最終工程を確定

出品処理を行う

完了カードが生成される

RefineRoom に戻る（編集不可）

5. 図面モードとの関係（Blueprint Link）
図面モードは FactoryRoom の内部構造を“線図化”して表示 している。

RefineRoom（図面モード）
　↓
FactoryRoom（形状データ・寸法データ）
　↓
RefineRoom（線図として表示）

図面は FactoryRoom の“実体”を反映

レバー操作で線図が即時変化

呼吸は弱く維持

6. 学習システムとの関係（Learning System）
FactoryRoom の学習システムは
RefineRoom の操作ログを吸収して賢くなる。

RefineRoom（操作）
　↓
FactoryRoom（ログ蓄積）
　↓
学習システム（傾向分析）
　↓
FactoryRoom（工程の最適化）
　↓
RefineRoom（プレビューが自然に良くなる）

RefineRoom は“操作”
FactoryRoom は“学習と最適化”。

7. 世界観の関係（Worldview Link）
● RefineRoom
静けさ

呼吸

白磁・真鍮・大理石

儀式具

感性の部屋

● FactoryRoom
巨大な機械

ライン

蒸気・鉄・真鍮

工程の音（UIには出さない）

実体の部屋

RefineRoom は“魂”
FactoryRoom は“身体”  
という関係。

8. 関係図（Diagram）

┌──────────────────────────────┐
│         RefineRoom（操作卓）         │
│  ・素材選択                         │
│  ・調整レバー                       │
│  ・図面モード                       │
│  ・保存／出品レバー                 │
└───────────────┬───────────────┘
                    │ 指示・数値・素材
                    ▼
┌──────────────────────────────┐
│        FactoryRoom（工場本体）        │
│  ・工程ライン                         │
│  ・機械処理                           │
│  ・確率アルゴリズム                   │
│  ・学習システム                       │
└───────────────┬───────────────┘
                    │ 結果・形状・質感
                    ▼
┌──────────────────────────────┐
│         RefineRoom（結果表示）        │
│  ・プレビュー                         │
│  ・図面表示                           │
│  ・呼吸アニメーション                 │
└──────────────────────────────┘

✔ 最短まとめ
RefineRoom＝操作卓

FactoryRoom＝工場本体

RefineRoom → FactoryRoom → RefineRoom の循環構造

保存・出品は FactoryRoom を経由する儀式

図面モードは FactoryRoom の形状データを線図化

学習システムは RefineRoom の操作ログを吸収

世界観：RefineRoom＝魂、FactoryRoom＝身体


