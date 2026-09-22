# Sticker Asset Library

天汐香弓の素材（ステッカー・アイコンなど）をまとめて管理するリポジトリです。
画像をフォルダに追加するだけで、ギャラリーページが自動更新されます。

**ギャラリー（公開後）:** `https://teshiokayumi.github.io/Sticker/`
※ 初回だけ下の「①GitHub Pagesを有効化」が必要です。

---

## 📁 フォルダ構成

```
Sticker/
├── stickers/   ← 手描き風の吹き出し・テキストステッカーなど
├── icons/      ← 正方形のアイコン・キャラクターイラストなど
├── docs/       ← 自動生成されるギャラリー（触らなくてOK）
└── scripts/    ← ギャラリーを作るスクリプト（触らなくてOK）
```

新しいカテゴリ（例: `banners/`, `headers/` など）を増やしたくなったら、
`scripts/build_gallery.py` の `CATEGORIES` に1行追加するだけで対応できます。

---

## ➕ 素材を増やす方法（GitHubだけで完結）

1. GitHubでこのリポジトリを開く
2. 追加したい種類のフォルダ（`stickers` か `icons`）を開く
3. **Add file → Upload files** をクリック
4. 画像をドラッグ＆ドロップ
5. 下の「Commit changes」ボタンを押す

これだけで、GitHub Actionsが自動的に動いて `docs/index.html`（ギャラリー）を
更新してくれます。1〜2分後にギャラリーを開くと新しい画像が反映されています。

### ファイル名のルール
- 半角英数字・ハイフンのみ（例: `you-got-this.png`, `halloween-boy.png`）
- 日本語・スペース・絵文字は避ける（表示は崩れませんが、URLが扱いにくくなります）
- ファイル名がそのままギャラリーのタイトルになります（ハイフンはスペースに変換されて表示）

---

## ①GitHub Pagesを有効化（最初の1回だけ）

1. リポジトリの **Settings → Pages**
2. **Source** を「Deploy from a branch」に設定
3. Branch を `main`、フォルダを `/docs` に設定して **Save**

数分後に `https://teshiokayumi.github.io/Sticker/` でギャラリーが見られるようになります。

---

## 🖼️ 現在の収録内容

- **stickers/** … `you-got-this.png`, `keep-going.png`, `go-for-it.png`
- **icons/** … `halloween-boy.png`

---

## 🔧 ローカルでギャラリーを再生成したい場合

```bash
python3 scripts/build_gallery.py
```

Python標準ライブラリのみで動作するので、追加インストールは不要です。
（普段はpushすれば自動実行されるので、手動実行はほぼ不要です）
