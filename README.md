# Sticker Asset Library

天汐香弓の素材（ステッカー・アイコンなど）をまとめて管理するリポジトリです。
画像をフォルダに追加するだけで、ギャラリーページが自動更新されます。

---

## ➕ 素材を増やす方法（GitHubだけで完結）
今後新しいステッカーやアイコンを追加したいときは、コードの <script> 内にある ASSETS_DATA 配列の中に以下の要領で1行追加するだけで自動で反映されます。
code
JavaScript
{
  id: 5,
  title: "新しい作品名",
  category: "ステッカー",
  type: "sticker",
  tags: ["タグ1", "タグ2"],
  image: "assets/ファイル名.png",
  format: "PNG",
  description: "説明文"
}

