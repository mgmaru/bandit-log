# bandit-log

[OverTheWire](https://overthewire.org/) の入門用 wargame **Bandit** を毎日少しずつ進め、その記録を残すためのリポジトリです。

## 目的

- Linux の基本コマンドに、実際に手を動かして慣れる
- 知らないコマンドを `man` で調べる癖をつける
- 「やりたいこと」から必要なコマンドを引けるメモを作り、障害対応のときに使えるようにする

## Bandit について

- 公式ページ: https://overthewire.org/wargames/bandit/
- 最初のレベル: https://overthewire.org/wargames/bandit/bandit0.html
- 各レベルで、次のレベルに SSH でログインするためのパスワードを探す形式
- 進捗はサイト側に保存されないため、このリポジトリで記録を管理する

## 接続方法

```
ssh bandit<レベル番号>@bandit.labs.overthewire.org -p 2220
```

例: Level 0 に接続する場合

```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

## 進め方

- 1日1レベル程度を目安に、無理なく続ける
- まず自分で調べて解く。調べ方は `man` → `tldr` → 検索の順
- 解いたら、その日のうちに `levels/` にメモを書く
- 使ったコマンドは `commands.md` に「やりたいこと」から引ける形で追記する

## ディレクトリ構成

```
bandit-log/
├── README.md
├── commands.md        # やりたいこと → コマンドの逆引きメモ
├── levels/
│   ├── level-00.md    # レベルごとの記録
│   ├── level-01.md
│   └── ...
└── .gitignore
```

## レベルごとのメモのテンプレート

`levels/level-XX.md` は次の形で書く。

```markdown
# Level XX → XX+1

## 目標
（公式ページに書かれている目標を自分の言葉で）

## 解き方
（何を考えて、どの順番で試したか）

## 使ったコマンド
- `コマンド`：何のために使ったか

## わからなかったこと・疑問
- （解けたあとも残っている疑問。あとで調べたら追記する）

## 学んだこと
- 
```

## コマンド逆引きメモ（commands.md）の書き方

コマンド名ではなく、「やりたいこと」を見出しにする。

```markdown
## ファイルの中身を見たい
- `cat ファイル名`
- `less ファイル名`：長いファイルをページ送りで見る

## 条件に合うファイルを探したい
- `find ディレクトリ -name 名前`
```

## パスワードの扱い

各レベルのパスワードはリポジトリに含めない。
手元の `passwords.txt` などに保存し、`.gitignore` で除外する。

```
# .gitignore
passwords.txt
```

## 進捗

| Level | 日付 | メモ |
|-------|------|------|
| 0 → 1 |      |      |
