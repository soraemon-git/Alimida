# 文法 v1.1

状態: 採用
対象バージョン: v1.1

## 1. 基本語順

基本語順は、主語を先に置き、述語や目的語を後ろに続ける形を基本とする。

```text
mi sena koda.
私はコードを学ぶ。

lu lito oto.
その人は音を聞く。
```

## 2. 標準形・許容形・非標準形

Alimida では、学習・教材・AI添削での一貫性を保つため、文法形を以下の3段階に分類する。

### 2.1 標準形

標準形は、教材・例文・公的な文章・AIの通常出力で使用する基本形である。学習者が最初に覚えるべき形であり、文法説明では標準形を中心に扱う。

### 2.2 許容形

許容形は、意味は通じるが、v1.1 の標準形としては扱わない形である。会話や学習途中の表現として理解できる場合があるが、教材の基本例文やAIの通常出力では標準形を使う。

許容形は誤りとはしない。ただし、AI添削では標準形を併記する。

### 2.3 非標準形

非標準形は、v1.1 の仕様では誤りとして扱う形である。AI添削では修正対象とする。

### 2.4 文法形の分類表

| 項目 | 標準形 | 許容形 | 非標準形 |
|---|---|---|---|
| Yes/No疑問文 | `ka yu sena koda?` | `yu sena koda ka?` | - |
| 疑問詞文 | `waka yu sena?` | `yu sena waka?` | - |
| 否定文 | `mi nu sena koda.` | - | `mi no sena koda.` |
| 否定返答 | `no, mi nu sena koda.` | - | `nu, mi nu sena koda.` |
| 過去否定 | `mi ta nu sena koda.` | - | `mi nu ta sena koda.` |
| 未来否定 | `mi fu nu pako buko.` | - | `mi nu fu pako buko.` |
| 名前表現 | `mi nama na Toshi.` | `mi nama Toshi.` | - |
| 所有表現 | `mi buko` | `buko de mi` | - |
| 移動先 | `mi golo to tomo.` | - | `mi golo tomo.` |
| 接続先 | `meka weno to data.` | - | `meka weno data.` |
| 受け手 | `mi deli buko to yu.` | - | `mi deli buko yu.` / `mi deli yu buko.` |
| 通常目的語 | `mi sena koda.` | - | `mi sena to koda.` |
| 内容対象 | `mi talo bo koda.` | - | `mi talo de koda.` |
| 所有 | `buko de yu` | - | `buko bo yu` を所有の意味で使う |
| 到達先疑問 | `to loka lu golo?` | `lu golo to loka?` / `loka lu golo?` | `loka lu golo to?` |
| 場所疑問 | `in loka yu pako koda?` | `yu pako koda in loka?` / `loka yu pako koda?` | `loka yu pako koda in?` |
| 起点疑問 | `fo loka yu kita?` | `yu kita fo loka?` / `loka yu kita?` | `loka yu kita fo?` |
| 受け手疑問 | `to homa yu deli buko?` | `yu deli buko to homa?` / `homa yu deli buko?` | `homa yu deli buko to?` |
| 内容疑問 | `bo waka yu talo?` | `yu talo bo waka?` / `waka yu talo?` | `waka yu talo bo?` |
| 同伴者疑問 | `we homa yu golo?` | `yu golo we homa?` / `homa yu golo?` | `homa yu golo we?` |
| 数量表現 | `dula buko` | - | `dula buko le` |
| 数量を含む名詞句 | `kono dula nava buko` | - | `kono dula nava buko le` |
| 数字の合成表記 | `dula deka una` | - | `duladekauna` |

上記の分類は v1.1 時点の運用基準である。将来的に、会話表現として一部の省略形を許容形へ移す可能性はあるが、v1.1 では学習しやすさとAI解析のしやすさを優先する。

## 3. 品詞体系

Alimida v1では、単語の品詞は基本語彙表で定義する。語尾だけで品詞を判定する一般規則は採用しない。

一部の語は関連語として似た語形を持つが、これは品詞変換規則ではない。たとえば、名詞 `nabi` と動詞 `nabo` は関連語として似た形を持つが、`-i` が名詞、`-o` が動詞であるという一般規則は導入しない。

| 品詞カテゴリ | 例 | 役割 |
|---|---|---|
| 代名詞 | `mi`, `yu`, `lu` | 人を指す |
| 指示語 | `kono`, `sono`, `ano` | 近い/遠い対象を指す |
| 名詞 | `humo`, `koda`, `nabi` | 人・物・概念を表す |
| 動詞 | `sena`, `pako`, `nabo` | 動作・変化を表す |
| 性質語（形容詞・副詞） | `meli`, `bano`, `nava`, `fasa`, `eza` | 性質・状態・様態を表す。位置によって形容詞的・副詞的・述語的に働く |
| 文法マーカー | `na`, `nu`, `ta`, `fu`, `ka`, `le` | 文の構造を示す |
| 返答語 | `ya`, `no` | Yes/No 疑問への返答を示す |
| 接続語 | `en`, `ba`, `do`, `si`, `dan` | 文や句をつなぐ |
| 関係語 | `in`, `de`, `fo`, `bi`, `bo`, `to`, `we`, `la`, `mo` | 場所・所有・起点・手段・内容・方向・話題・付加を示す |
| 疑問詞 | `waka`, `loka`, `modo` | 質問の焦点を示す |

各単語の品詞は [04_vocabulary_core100.md](./04_vocabulary_core100.md) の基本語彙表を基準とする。

## 4. 名詞句と修飾

### 4.1 形容詞による名詞修飾

性質語が名詞を修飾する場合は、性質語を名詞の前に置く。

```text
nava buko
新しい本

bano ela
大きい空

meli nabi
良い案内
```

### 4.2 指示語・形容詞・名詞・複数の順序

指示語、形容詞、名詞、複数表現を組み合わせる場合は、以下の順序を推奨する。

```text
指示語 + 形容詞 + 名詞 + le
```

例:

```text
kono nava buko le
これらの新しい本

sono bano meka le
それらの大きい機械
```

## 5. 性質語

Alimida の性質語は、性質・状態・様態・評価を表す語である。性質語は、置かれる位置によって働きが変わる。

### 5.1 名詞を修飾する場合

名詞を修飾する場合、性質語は名詞の前に置く。

```text
nava buko
新しい本

fasa humo
速い人

eza koda
簡単なコード
```

### 5.2 動作を修飾する場合

動作を修飾する場合、性質語は動詞句の後ろに置く。

```text
mi golo fasa.
私は速く行く。

mi pako koda eza.
私はコードを簡単に作る。

meka weno to data fasa.
機械がデータに速く接続する。

lu lito oto meli.
その人は音をよく聞く。
```

性質語を動詞の前に置いて副詞的に使う形は、v1.1 では非標準とする。

```text
非標準:
mi fasa golo.
mi eza pako koda.
```

### 5.3 主語の性質を述べる場合

主語の性質を述べる場合、`na` の後ろに性質語を置く。

```text
lu na fasa.
その人は速い。

koda na eza.
コードは簡単だ。

meka na weka.
機械は弱い。

sede na meli.
学習は良い。
```

### 5.4 形容詞用法と副詞用法の違い

```text
mi pako eza koda.
私は簡単なコードを作る。

mi pako koda eza.
私はコードを簡単に作る。
```

性質語が名詞の前にある場合は名詞を修飾し、動詞句の後ろにある場合は動作全体を修飾する。

## 6. 数量表現

数量を表す場合、数を名詞の前に置く。

```text
数 + 名詞
```

例:

```text
una buko
1冊の本

dula buko
2冊の本

deka una buko
11冊の本
```

数字がある場合、複数マーカー `le` は通常使わない。

```text
標準:
dula buko

非標準:
dula buko le
```

`le` は、具体的な数を示さず、複数であることだけを示す場合に使う。

```text
buko le
本たち / 複数の本

dula buko
2冊の本
```

指示語・数量・性質語・名詞を組み合わせる場合は、以下の順序を標準形とする。

```text
指示語 + 数量 + 性質語 + 名詞
```

例:

```text
kono dula nava buko
この2冊の新しい本
```

合成数字は、スペースで区切って表記する。

```text
標準:
dula deka una

非標準:
duladekauna
```

数字体系の詳細は [06_vocabulary_basic_systems.md](./06_vocabulary_basic_systems.md) を参照する。

## 7. 基本体系語彙の文法メモ

基本体系語彙は [06_vocabulary_basic_systems.md](./06_vocabulary_basic_systems.md) で管理する。v1.1 では、数字、方向・位置、色、数量・程度、時間・日付の基礎を採用済みの基本体系語彙として扱う。

ただし、9999 を超える大きな数、序数、完全な日付表記、時刻表記、曜日名、月名、方角語などは後の拡張で扱う。

### 7.1 数量表現

数字と数量語は、名詞の前に置く。

```text
数字 + 名詞
数量語 + 名詞
```

例:

```text
dula buko
2冊の本

muta buko
多くの本
```

具体的な数がある場合、`le` は通常使わない。

```text
標準:
dula buko

非標準:
dula buko le
```

`zeno` は数量0を表す数字語である。v1.1 では、「存在しない」「所有していない」「ない」を表す一般的な否定表現としては扱わない。これらの表現は、存在表現・所有表現の整理と合わせて後のバージョンで検討する。

### 7.2 位置句の構造

位置句は、次の構造を使う。

```text
参照名詞 + 位置名詞
```

関係語は位置句の外側に置く。

```text
mi in tomo feni.
私は家の前にいる。

mi golo to tomo feni.
私は家の前へ行く。

mi kita fo tomo feni.
私は家の前から来る。
```

`de` は空間位置には使わない。`de` は所有・所属のみを表す。

### 7.3 色語

色語は性質語とする。既存の性質語ルールに従う。

```text
色語 + 名詞
名詞 + na + 色語
```

例:

```text
ledo buko
赤い本

buko na ledo.
本は赤い。
```

### 7.4 程度語と性質語

程度語は、性質語の前に置いて性質語を修飾する。

```text
程度語 + 性質語
```

例:

```text
hano bano meka
とても大きい機械

lili weka meka
少し弱い機械
```

v1.1 では、程度語は性質語の前に置いて、性質語を修飾する語として扱う。程度語が動作句全体を修飾する用法は、v1.1 では正式採用しない。必要であれば v1.2 以降で検討する。

### 7.5 時間・日付の基礎

時間語は、文頭に置いて文全体の時間文脈を示せる。

```text
時間語 + 文
```

例:

```text
kodeyo mi sena koda.
今日、私はコードを学ぶ。

fudeyo mi fu pako buko.
明日、私は本を作る予定だ。
```

完全な日付表記、時刻表記、曜日名、月名は、後のバージョンで検討する。

## 8. 目的語

基本的な他動詞文は、主語、動詞、目的語の順に置く。

```text
主語 + 動詞 + 目的語
```

例:

```text
mi sena koda.
私はコードを学ぶ。

mi pako buko.
私は本を作る。

lu lito oto.
その人は音を聞く。

yu yuta koda.
あなたはコードを使う。
```

## 9. 所有・所属

所有・所属は、標準形と明示形を併用する。

### 9.1 標準形: 所有者 + 名詞

短く基本的な所有・所属は、所有者を名詞の前に置いて表す。

```text
所有者 + 名詞
```

例:

```text
mi nama
私の名前

yu buko
あなたの本

lu tomo
その人の家
```

### 9.2 許容形・明示形: 名詞 + de + 所有者

所有関係を明示したい場合、または語のまとまりが曖昧になる場合は、`de` を使う。

```text
名詞 + de + 所有者
```

例:

```text
nama de mi
私の名前

buko de yu
あなたの本

tomo de lu
その人の家
```

### 9.3 使い分け

標準形は短く、初級文や日常的な所有表現に向く。明示形は、所有・所属の関係を強調したい場合や、語のまとまりを明確にしたい場合に使う。

```text
mi nama na Toshi.
私の名前はToshiです。

nama de mi na Toshi.
私の名前はToshiです。
```

会話上の自然さを優先する場合は、`mi nama Toshi.` も許容する。ただし、学習用の標準例文では `na` を明示する。

### 9.4 `de` の用法制限

`de` は所有・所属を表す関係語として使う。

```text
名詞 + de + 所有者
```

例:

```text
nama de mi
私の名前

buko de yu
あなたの本

tomo de lu
その人の家
```

v1.1 以降、`de` は「〜から」「〜によって」「〜について」の意味では使用しない。これらの意味は、それぞれ `fo`, `bi`, `bo` を使って表す。

## 10. be動詞的表現 `na`

`na` は「〜である」を表す be動詞的な要素として使う。

```text
mi na humo.
私は人です。

ela na bano.
空は大きい。
```

## 11. 否定 `nu`

`nu` は否定を表す文法マーカーである。否定したい述語の前に置くことを基本とする。

```text
mi nu selo sima.
私は意味を知らない。

lu nu lito oto.
その人は音を聞かない。

yu nu suki noka.
あなたは夜が好きではない。
```

`nu` は文中で述語を否定するために使う。Yes/No 疑問への返答には使わない。

```text
ka yu sena koda?
no, mi nu sena koda.
いいえ、私はコードを学ばない。
```

`no` は返答語「いいえ」であり、文中否定には使わない。

```text
非標準:
mi no sena koda.

標準:
mi nu sena koda.
```

| 表現 | 意味 | 判定 | 説明 |
|---|---|---|---|
| `ya.` | はい | 標準 | 肯定返答 |
| `no.` | いいえ | 標準 | 否定返答 |
| `mi nu sena koda.` | 私はコードを学ばない | 標準 | 文中否定 |
| `mi no sena koda.` | 私はコードを学ばない | 非標準 | `no` を文中否定に使っている |
| `no, mi nu sena koda.` | いいえ、私はコードを学ばない | 標準 | 返答語 + 文中否定 |
| `nu, mi nu sena koda.` | いいえ、私はコードを学ばない | 非標準 | `nu` を返答語に使っている |

## 12. 時制

時制は、動詞または述語の前に時制マーカーを置いて表す。

### 12.1 過去 `ta`

`ta` は過去を表す。

```text
mi ta sena koda.
私はコードを学んだ。

lu ta golo to tomo.
その人は家へ行った。
```

### 12.2 未来 `fu`

`fu` は未来を表す。

```text
mi fu pako buko.
私は本を作る予定だ。

ka yu fu weno to data?
あなたはデータに接続する予定ですか？
```

### 12.3 時制と否定の組み合わせ

時制マーカーと否定マーカーが共存する場合は、以下の語順を標準形とする。

```text
主語 + 時制 + nu + 動詞 + 目的語
```

例:

```text
mi ta nu sena koda.
私はコードを学ばなかった。

lu ta nu lito oto.
その人は音を聞かなかった。

mi fu nu pako buko.
私は本を作らない予定です。
```

時制を先に示し、その後に `nu` を置くことで、時間情報と否定対象を明確にする。

```text
非標準:
mi nu ta sena koda.
mi nu fu pako buko.
```

`主語 + nu + 時制 + 動詞` の語順は v1.1 では非標準とする。

## 13. 疑問文

疑問文では、疑問マーカーまたは疑問詞を文頭に置く形を標準形とする。

### 13.1 Yes/No疑問 `ka`

Yes/No疑問文では、疑問マーカー `ka` を使用する。

標準形:

```text
ka yu sena koda?
あなたはコードを学びますか？
```

許容形:

```text
yu sena koda ka?
あなたはコードを学びますか？
```

`ka` は文頭に置くことを標準とする。文頭 `ka` は、聞き手に文の最初で疑問文であることを知らせる。

短い文、確認、聞き返し、会話上の自然さを優先する場合は、`ka` を文末に置いてもよい。ただし、教材・例文・AI通常出力では文頭 `ka` を使用する。

### 13.2 Yes/No 疑問への返答

Yes/No 疑問への返答には、肯定返答 `ya` と否定返答 `no` を使う。

```text
ya = はい
no = いいえ
```

例:

```text
ka yu sena koda?
ya, mi sena koda.
あなたはコードを学びますか？
はい、私はコードを学びます。

ka yu sena koda?
no, mi nu sena koda.
あなたはコードを学びますか？
いいえ、私はコードを学びません。
```

`no` は返答語であり、文中の否定には使わない。文中の否定には `nu` を使う。

```text
非標準:
mi no sena koda.

標準:
mi nu sena koda.
```

### 13.3 疑問詞

疑問詞も文頭に置くことを推奨する。

Alimida v1.1 では、以下の疑問詞セットを使用する。

| 語 | 意味 | 役割 |
|---|---|---|
| `waka` | 何 | 物・内容を問う |
| `homa` | 誰 | 人を問う |
| `loka` | どこ | 場所を問う |
| `tima` | いつ | 時点・時期を問う |
| `nalo` | なぜ | 理由を問う |
| `modo` | どう | 方法・様態を問う |
| `delo` | どれ・どの | 選択肢を問う |

例:

```text
waka yu sena?
あなたは何を学びますか？

homa weno to yu?
誰があなたに接続しますか？

to loka lu golo?
その人はどこへ行きますか？

tima yu sena?
あなたはいつ学びますか？

nalo yu nu suki koda?
なぜあなたはコードが好きではないのですか？

modo mi pako koda?
私はどうやってコードを作りますか？
```

`tima` は疑問詞「いつ」であり、名詞「時・時間」ではない。名詞「時・時間」は `temo` を使う。

```text
tima yu sena?
あなたはいつ学びますか？

mi nidi temo.
私は時間が必要です。
```

疑問詞を文末に置く形も意味は通じるため許容形とする。ただし、教材・例文・AI通常出力では文頭疑問詞を使用する。

```text
yu sena waka?
あなたは何を学びますか？

yu pako koda in loka?
あなたはどこでコードを作りますか？
```

### 13.4 関係語つき疑問詞

`to`, `in`, `fo`, `bo`, `we` などの関係語を伴う疑問詞では、関係語と疑問詞をセットにして文頭に置く形を標準形とする。

```text
to loka lu golo?
その人はどこへ行きますか？

in loka yu pako koda?
あなたはどこでコードを作りますか？

fo loka yu kita?
あなたはどこから来ますか？

to homa yu deli buko?
あなたは誰に本を渡しますか？

bo waka yu talo?
あなたは何について話しますか？

we homa yu golo?
あなたは誰と行きますか？
```

関係語句を通常の位置に置く形も許容形とする。

```text
lu golo to loka?
yu pako koda in loka?
yu kita fo loka?
yu deli buko to homa?
yu talo bo waka?
yu golo we homa?
```

関係語を省略し、疑問詞だけを文頭に置く形は、関係が動詞の構文型または文脈から明確な場合に限り会話許容とする。

```text
loka lu golo?
loka yu pako koda?
homa yu deli buko?
waka yu talo?
```

疑問詞だけを文頭に出し、関係語だけを文末に残す形は非標準とする。

```text
非標準:
loka lu golo to?
homa yu deli buko to?
waka yu talo bo?
```

教材・例文・AI通常出力では、関係語を明示する標準形を使う。

### 13.5 文頭標準・文末許容

Yes/No疑問の `ka` と疑問詞は、文頭配置を標準形とし、文末配置を許容形とする。

- 文頭配置: 音声会話で文の早い段階から疑問文であることを示しやすい。
- 文末配置: 短い確認や自然な会話で使いやすい。

### 13.6 語尾上げ

疑問文では、文末を軽く上げる発音を推奨する。ただし、疑問の意味は語尾上げだけではなく、`ka` または疑問詞によって明示することを基本とする。

## 14. 複数表現 `le`

複数表現には `le` を使用する。

```text
le = 複数を表す要素
```

### 14.1 代名詞・指示語では接尾語

代名詞・指示語では、`le` は接尾語として結合する。

| 単数 | 複数 | 意味 |
|---|---|---|
| mi | mile | 私たち |
| yu | yule | あなたたち |
| lu | lule | その人たち |
| kono | konole | これら |
| sono | sonole | それら |
| ano | anole | あれら |

これらの複数形は規則的に作れるため、基本100語には含めない派生語として扱う。

### 14.2 一般名詞では独立マーカー

一般名詞では、`le` は独立した複数マーカーとして名詞の後ろに置く。

| 単数 | 複数 | 意味 |
|---|---|---|
| humo | humo le | 人々 |
| buko | buko le | 複数の本 |
| koda | koda le | 複数のコード |
| meka | meka le | 複数の機械 |

### 14.3 指示語が名詞を修飾する場合

指示語が名詞を修飾する場合は、名詞側の `le` で複数を表すことを基本とする。

```text
kono buko le
これらの本

sono humo le
その人たち

ano meka le
あの機械たち
```

指示語を単独で使う場合は、`le` を接尾語として結合できる。

```text
konole
これら

sonole
それら

anole
あれら
```

## 15. 接続語・前置詞的機能語

文法・機能語として、以下を使用する。

| 語 | 意味 | 用途 |
|---|---|---|
| en | そして | and |
| ba | しかし | but |
| do | だから・それで | so / therefore |
| si | もし | if |
| dan | その時・ならば | then |
| in | 〜の中・〜で | in / at |
| de | 〜の | 所有・所属 |
| fo | 〜から | 起点・由来 / from |
| bi | 〜によって・〜で | 行為者・手段 / by |
| bo | 〜について | 内容・対象 / about |
| to | 到達点・方向・受け手・接続先 | 動作が向かう先 |
| we | 〜と一緒に | with |
| la | 〜については | 文全体の話題・文脈マーカー |
| mo | 〜も・また | also |

## 16. 到達点・方向・受け手 `to`

`to` は、動作が向かう先を表す関係語である。移動先、到達先、接続先、送付先、授与先、発話の相手などを表す。

```text
to = 到達点・方向・受け手・接続先
```

`to` は日本語の「に」「へ」と完全に対応する語ではない。Alimida では、動作が何かに向かう場合に `to` を使う。

例:

```text
mi golo to tomo.
私は家へ行く。

meka weno to data.
機械がデータに接続する。

mi deli buko to yu.
私はあなたに本を与える。

mi talo to yu.
私はあなたに話す。
```

v1.1 では、移動先・接続先・受け手など、動作が向かう先を表す場合は `to` を必須とする。

### 16.1 `to` を使う場合

`to` は、動作が向かう先を表す場合に使う。

```text
golo to tomo
家へ行く

weno to data
データに接続する

deli buko to yu
あなたへ本を与える

talo to yu
あなたに話す
```

### 16.2 `to` を使わない場合

普通の目的語には `to` を使わない。

```text
mi sena koda.
私はコードを学ぶ。

mi pako buko.
私は本を作る。

lu lito oto.
その人は音を聞く。

mi lisu buko.
私は本を読む。
```

これらは、動作が対象へ向かうというより、動詞が直接対象を取る文である。

### 16.3 判断基準

`to` が必要か迷う場合は、以下のように考える。

```text
動作が「どこへ」「誰へ」「何へ」向かうかを表すなら to
動詞が直接「何を」するかを表すなら目的語
```

例:

```text
mi golo to tomo.
私は家へ行く。
```

`tomo` は「行く」という動作の到達先なので `to` を使う。

```text
mi pako buko.
私は本を作る。
```

`buko` は「作る」という動作の目的語なので `to` は使わない。

### 16.4 標準・非標準の比較

| 表現 | 意味 | 判定 | 説明 |
|---|---|---|---|
| `mi pako buko.` | 私は本を作る | 標準 | `buko` は目的語 |
| `mi pako to buko.` | 私は本へ作る | 非標準 | 普通の目的語に `to` を付けている |
| `mi golo to tomo.` | 私は家へ行く | 標準 | `tomo` は到達先 |
| `mi golo tomo.` | 私は家へ行く | 非標準 | 到達先に `to` がない |
| `meka weno to data.` | 機械がデータに接続する | 標準 | `data` は接続先 |
| `meka weno data.` | 機械がデータに接続する | 非標準 | 接続先に `to` がない |
| `mi deli buko to yu.` | 私はあなたに本を与える | 標準 | `yu` は受け手 |
| `mi deli yu buko.` | 私はあなたに本を与える | 非標準 | 二重目的語構文は使わない |

## 17. 動詞の構文型

Alimida では、動詞ごとに基本的な構文型を定義する。構文型は、動詞がどのような要素を必要とするかを示す。

例:

```text
sena + 目的語
pako + 目的語
golo + to + 到達先
weno + to + 接続先
deli + 物 + to + 受け手
talo + to + 相手
talo + bo + 内容
```

構文型は [04_vocabulary_core100.md](./04_vocabulary_core100.md) の語彙表に記載する。これにより、英語のように「この動詞は to が必要かどうか」を個別に推測するのではなく、語彙表で確認できるようにする。

## 18. 起点・由来 `fo`

`fo` は「〜から」を表す関係語である。場所・人・情報源・由来など、何かの出発点や起点を表す。

```text
A fo B
A は B から / B 由来の A
```

例:

```text
mi kita fo tomo.
私は家から来る。

mi teka buko fo yu.
私はあなたから本を受け取る。

luma kita fo data.
情報はデータから来る。
```

`fo` は所有を表さない。所有・所属には `de` を使う。

```text
buko de yu
あなたの本

buko fo yu
あなたからの本
```

v1.1 では、`fo` を原因表現全般には広げない。抽象的な原因用法は未定義とし、今後検討する。

## 19. 行為者・手段 `bi`

`bi` は「〜によって」「〜で」を表す関係語である。行為者、作成者、実行主体、または手段を表す。

```text
A bi B
B による A / B で A
```

例:

```text
teto bi mi
私による文

koda bi meka
機械によるコード

mi pako teto bi meka.
私は機械で文を作る。

teto bi AI na meli.
AIによる文は良い。
```

`bi` は起点を表さない。「〜から」を表す場合は `fo` を使う。`bi` は所有も表さない。所有・所属には `de` を使う。

v1.1 では、`bi` は行為者・作成者・手段・道具に限定する。「雨によって濡れた」のような原因表現は未定義とし、今後検討する。

## 20. 内容・対象 `bo`

`bo` は「〜について」を表す関係語である。話す、書く、読む、考える、学ぶ、尋ねるなどの内容・対象を表す。

```text
A bo B
B についての A
```

例:

```text
mi talo bo koda.
私はコードについて話す。

mi tebo teto bo sede.
私は学習についての文を書く。

mi omo bo yume.
私は夢について考える。

teto bo sede na meli.
学習についての文は良い。

buko bo AI na nava.
AIについての本は新しい。
```

`bo` は所有を表さない。所有・所属には `de` を使う。`bo` は起点も表さない。起点・由来には `fo` を使う。

```text
buko de yu
あなたの本

buko bo yu
あなたについての本

buko fo yu
あなたからの本
```

## 21. `bo` と `la` の使い分け

`bo` と `la` は、どちらも日本語では「〜について」と訳せる場合があるが、文法上の役割は異なる。

- `bo` は、文中の内容・対象を表す。
- `la` は、文全体の話題・文脈を提示する。

`bo` は、話す・書く・読む・考える・学ぶ・尋ねるなどの対象を表すときに使う。

```text
mi talo bo koda.
私はコードについて話す。
```

この文では、`bo koda` は `talo` の内容・対象を表す。

`la` は、文の最初などで大きな話題を提示するときに使う。

```text
koda la, mi nu selo.
コードについては、私は知らない。
```

この文では、`koda la` が文全体の話題である。

`bo` と `la` は併用できる。

```text
koda la, mi talo bo AI.
コードについては、私はAIについて話す。
```

この文では、`koda la` は文全体の話題であり、`bo AI` は `talo` の内容・対象である。

## 22. AI添削・教材運用での扱い

Alimida のAI添削では、文法形を以下のように扱う。

### 22.1 標準形

標準形はそのまま正しい形として扱う。AIの通常出力でも標準形を使う。

### 22.2 許容形

許容形は誤りとはしない。ただし、学習者には標準形を併記する。

```text
入力:
yu sena koda ka?

添削:
意味は通じます。標準形では `ka yu sena koda?` とします。
```

### 22.3 非標準形

非標準形は修正対象とする。AIは理由と標準形を示す。

```text
入力:
mi no sena koda.

添削:
`no` は返答語です。文中の否定には `nu` を使います。
標準形: mi nu sena koda.
```

### 22.4 AI通常出力

AIが Alimida 文を生成する場合、原則として標準形のみを使う。許容形は、ユーザー入力の理解や比較説明でのみ扱う。

## 23. 今後の拡張項目

v1.1 では採用しない項目や後の拡張で扱う項目は、[91_todo.md](./91_todo.md) を参照する。
