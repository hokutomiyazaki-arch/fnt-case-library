# FNT症例ライブラリ

臨床シェア会に持ち寄られた症例を、ヒストリー → 仮説 → アセスメント → リアセスメント → アウトカムの
5段で読むためのWebアプリ。疑った神経系・クライアント種別・アウトカム・仮説の的中・開催回で絞り込め、
主訴やドリル名で全文検索できる。

**公開URL：** https://hokutomiyazaki-arch.github.io/fnt-case-library/

FNTニューロコミュニティの「オリジナルアプリ」コースからリンクして会員に配る。
他のアプリ（n-back・リズムファイター・VOR・OKN 等）と同じ置き方。

## 中身

依存ゼロの**単体HTML 1枚**（`index.html`）。データもCSSもJSも全部この中。
ビルドもサーバーも要らない。

| 開催回 | 件数 |
|---|---|
| 2026夏 ランチミートアップ 7/12 | 10件（FNT-1〜10） |
| 2026秋 臨床シェア会 9/13 | 10件（FNT-11〜20） |

## 🔴 正本はここではない

**正本は `fnt-neuro-community/case-library/`（private）。** ここはそのコピーを配信するだけ。

| | 場所 |
|---|---|
| 正本（原資料との対応・実測メモ・作業の経緯） | `~/dev/fnt-neuro-community/case-library/` |
| 配信（ここ） | `fnt-case-library`（public・GitHub Pages） |

`ws/`（応用実践WS資料）の正本＝`fnt-neuro-community` ／ 配信＝`fnt-ws-slides` と同じ分け方。

## 🔴 このリポジトリは public

**入れてよいのは `index.html` だけ。** 次のものは絶対に入れない。

- 手書きシートの**写真そのもの**（記入者の実名が写っている）
- クライアントの氏名（アプリ内は年代・性別のみ。氏名は元から持っていない）
- 発表者の実名（アプリ内は**イニシャル表記**。原本の記名は Drive にある）
- Drive / Notion の**認証情報**（リンクは貼ってあるが、アクセス権がある人しか開けない）

## 更新のしかた

1. 正本 `fnt-neuro-community/case-library/index.html` の `CASES` 配列に症例を足す
2. ここへコピーして push（GitHub Pages は push から1〜2分で反映）

```bash
cp ~/dev/fnt-neuro-community/case-library/index.html ~/dev/fnt-case-library/index.html
cd ~/dev/fnt-case-library && git add index.html && git commit -m "症例を追加" && git push
```
