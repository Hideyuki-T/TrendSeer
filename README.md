## 名称：TrendSeer

## 🧰 技術スタック / Tech Stack
#### 言語・IDE
![Pine Script](https://img.shields.io/badge/Pine%20Script-v5-green?logo=tradingview&style=for-the-badge)
![PhpStorm](https://img.shields.io/badge/PhpStorm-143?style=flat&logo=phpstorm&logoColor=white)
#### パッケージ・バージョン管理
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)

## 概要：
- TradingView 上に描画する

## 目的：
- 毎回手作業で"トレンドライン・水平線"を引くことが面倒だったのでそれを自動化している。

## コード説明　：
### yearHighLow.pine :
<table>
<tr>
<th>処理</th><th>内容</th>
</tr>
<tr>
<th>request.security(..., "12M", high)</th><th>現在の年足の高値を取得</th>
</tr>
<tr>
<th>request.security(..., "12M", low)</th><th>現在の年足の安値を取得</th>
</tr>
<tr>
<th>ta.highest(..., 5)</th><th>過去5年の最高値を取得</th>
</tr>
<tr>
<th>ta.lowest(..., 5)</th><th>過去5年の最安値を取得</th>
</tr>
<tr>
<th>if 現在の年 > 過去最高なら</th><th>水平線を引く</th>
</tr>
<tr>
<th>if 現在の年 < 過去最低なら</th><th>水平線を引く</th>
</tr>
<tr>
<th>line.new(...)</th><th>水平線を右方向に引く</th>
</tr>
</table>

## 使い方：
- Copy and Paste で Pine エディタに貼り付けて実行<br>
※ TradingView に GitHub の連携 API が存在しない為。

## 現在の課題：
- 年足〜時間足までの"トレンドライン & レジサポライン"を正確に引けるようにすること。

### 現在の目的地：
- 毎月安定して10万円を稼げるようになること

### 次の目的地：
- 毎月安定して100万円を稼げるようになること
