# 名称：TrendSeer 🕊

## 🧰 技術スタック / Tech Stack：
#### 言語・IDE
![Pine Script](https://img.shields.io/badge/TradingView-Pine%20Script%20v5-blue?logo=tradingview&style=for-the-badge)
![PhpStorm](https://img.shields.io/badge/PhpStorm-143?style=flat&logo=phpstorm&logoColor=white)
#### パッケージ・バージョン管理
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)


## 概要：
本リポジトリでは、TradingView 上にて表示できる以下2系統のインジケーターを提供しています：

1. **マルチタイムフレーム対応インジケーター（MTF）**  
　　─ 1つのスクリプトで、複数の時間足（年足〜1分足）を同時に描画・管理できます。

2. **単一時間足インジケーター（個別版）**  
　　─ それぞれの時間足（例：週足・日足など）に特化した軽量なシングルスクリプトです。


## 🧩 MTF版：特徴：
- 年足、月足、週足、日足、4時間足…など **8つの時間足に対応**
- 各時間足ごとに：
    - 「表示ON/OFF」
    - 「高値バー数 / 安値バー数」を個別設定可能
- 実際に高値・安値が発生したバーから **未来方向に水平レイ** を描画
- 各時間足ごとに **常に1本のライン**を維持（自動更新）
- Pine Script v5、`dynamic_requests=true` を活用


## 🔹 単体版：特徴：
- 各時間足（例：週足、日足、1時間足）に専用化された軽量スクリプト
- 「現在足の高値・安値」が「過去N本の最高値・最安値」をブレイクした場合のみラインを描画
- ラインは未来方向に水平レイとして表示
- 描画条件を満たしたときだけ描かれる **一時的なサイン的要素** にも応用可能


## 🧪 利用例：
- 複数時間足からのサポレジ水準確認
- 戦略的ブレイクポイントの自動可視化
- 複雑な時間構造の補助ツールとして活用（特にフラクタル/マルチフレーム分析）


## 🚀 使い方：

### 〜 MTF版 〜
1. TradingView の Pineエディタにスクリプトを貼り付け
2. 好みの時間足を `true` に切り替え
3. 各時間足ごとの過去バー数（高・安）を指定
4. チャート上に水平レイが表示されます

### 〜 単体版 〜
1. 使用したい時間足用のスクリプトをエディタに貼り付け
2. `past_high`, `past_low` のパラメータを調整
3. 現在足が過去水準をブレイクした時、ラインが描画されます


## 構成　：
```
.
├── horizontal_line
│   ├── 15minHighLow.pine
│   ├── 1hHighLow.pine
│   ├── 1minHighLow.pine
│   ├── 4hHighLow.pine
│   ├── 5minHighLow.pine
│   ├── dayHighLow.pine
│   ├── MTF_HighLow.pine
│   ├── weekHighLow.pine
│   └── yearHighLow.pine
└── README.md
```

