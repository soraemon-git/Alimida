# Basic Systems Vocabulary v1.1

## 1. 目的

この文書は、Alimida の基本体系語彙を定義する。

基本体系語彙とは、数字・方向・色・量・時間など、単独語彙というより体系としてまとめて覚える語彙群である。

Core Vocabulary 100+α とは分けて管理し、必要に応じて段階的に拡張する。

## 2. 数字体系

### 2.1 基本方針

Alimida の数字体系は 10進法とする。

```text
0〜9 は個別語
10 / 100 / 1000 も個別語
11 = 10 + 1 型
20 = 2 + 10 型
21 = 2 + 10 + 1 型
数量語順 = 数 + 名詞
数字がある場合 le は不要
```

### 2.2 基本数字語

| 数 | Alimida | 読み | 備考 |
|---:|---|---|---|
| 0 | `zeno` | ゼノ | zero 系 |
| 1 | `una` | ウナ | uno / uni 系 |
| 2 | `dula` | ドゥラ | duo / dual 系 |
| 3 | `tela` | テラ | tri / three 系 |
| 4 | `fola` | フォラ | four 系 |
| 5 | `pema` | ペマ | penta 系を短く Alimida 化 |
| 6 | `sika` | シカ | six 系 |
| 7 | `sepa` | セパ | sept 系 |
| 8 | `oka` | オカ | oct 系 |
| 9 | `nona` | ノナ | non-/nine 系 |
| 10 | `deka` | デカ | deca 系 |
| 100 | `sento` | セント | cent 系 |
| 1000 | `kilo` | キロ | kilo 系 |

5 は `peta` ではなく `pema` とする。`peta` は SI 接頭辞 `peta-` と混同される可能性があるため採用しない。

### 2.3 合成規則

```text
11 = deka una
20 = dula deka
21 = dula deka una
100 = sento
200 = dula sento
1000 = kilo
2000 = dula kilo
```

例:

```text
35 = tela deka pema
99 = nona deka nona
125 = sento dula deka pema
256 = dula sento pema deka sika
2026 = dula kilo dula deka sika
```

合成数字はスペースで区切って表記する。

```text
標準:
dula deka una

非標準:
duladekauna
```

### 2.4 数量表現

数量は名詞の前に置く。

```text
dula buko
2冊の本

deka una buko
11冊の本
```

数字がある場合、`le` は不要である。

```text
標準:
dula buko

非標準:
dula buko le
```

### 2.5 名詞句内の位置

指示語・数量・性質語・名詞を組み合わせる場合、以下の語順を標準形とする。

```text
指示語 + 数量 + 性質語 + 名詞
```

例:

```text
kono dula nava buko
この2冊の新しい本
```

### 2.6 v1.1 で保留する項目

序数、日付、時刻、10,000 以上の表現は v1.1 では正式採用せず、今後検討する。

## 3. 今後追加予定の体系語彙

```text
方向・位置
色
量・程度
時間・日付
身体
家族
生活基本語
```