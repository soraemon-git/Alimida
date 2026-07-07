# 関係語一覧

状態: v1.2 教材用

この文書は、関係語を教材向けに整理する一覧表である。正式な文法仕様は [03_grammar.md](./03_grammar.md) を正とする。

## 対象語

| 関係語 | 役割 | 標準例文 | 日本語訳 | 似ている語との違い | よくある誤り |
|---|---|---|---|---|---|
| to | 到達点・方向・受け手・接続先 | mi golo to tomo. | 私は家へ行く。 | 通常目的語には使わない。動作が向かう先に使う。 | mi golo tomo. |
| in | 場所・内部・そこで | mi in tomo. | 私は家にいる。 | 到達点ではなく、場所を表す。 | mi golo in tomo. |
| de | 所有・所属 | buko de yu na nava. | あなたの本は新しい。 | `fo` は起点、`bi` は行為者・手段を表す。 | buko bo yu na nava. |
| fo | 起点・由来 | mi kita fo tomo. | 私は家から来る。 | 所有には使わない。原因表現全般には広げない。 | buko fo yu を「あなたの本」の意味で使う。 |
| bi | 行為者・手段 | mi pako teto bi meka. | 私は機械で文を作る。 | `fo` は起点、`de` は所有・所属を表す。 | teto de mi を「私による文」の意味で使う。 |
| bo | 内容・対象 | mi talo bo koda. | 私はコードについて話す。 | `la` は文全体の話題を示す。 | mi talo de koda. |
| we | 同伴 | mi golo we yu. | 私はあなたと一緒に行く。 | 受け手には `to` を使う。 | mi deli buko we yu. |
| la | 話題・文脈 | koda la, mi talo bo sede. | コードについては、私は学習について話す。 | `bo` は文中の内容・対象を表す。 | mi la koda talo. |
| mo | 追加 | yu mo sena koda. | あなたもコードを学ぶ。 | `we` は同伴、`mo` は追加を表す。 | mi golo mo yu. |

## 学習上の注意

### `to` と通常目的語

`to` は、移動先・接続先・受け手など、動作が向かう先を表す場合に使う。普通の目的語には使わない。

```text
標準:
mi golo to tomo.
mi sena koda.

非標準:
mi golo tomo.
mi sena to koda.
```

### `de`, `fo`, `bi`, `bo`

日本語では似た訳になる場合があるが、Alimida では役割を分ける。

```text
buko de yu
あなたの本

buko fo yu
あなたからの本

buko bi yu
あなたによる本

buko bo yu
あなたについての本
```

### `bo` と `la`

`bo` は文中の内容・対象を表す。`la` は文全体の話題・文脈を示す。

```text
mi talo bo koda.
私はコードについて話す。

koda la, mi talo.
コードについては、私は話す。
```

### 関係語つき疑問詞

教材用の標準形では、関係語と疑問詞をセットで文頭に置く。

```text
to loka lu golo?
その人はどこへ行きますか？

bo waka yu talo?
あなたは何について話しますか？
```

関係語だけを文末に残す形は非標準である。
