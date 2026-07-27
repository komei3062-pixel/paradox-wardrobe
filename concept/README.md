# コンセプトブック — ソース

`paradox-wardrobe-concept.html` は「パラドックス・ワードローブ」ブランドコンセプトブック（全8頁・A4）のHTMLソースです。テーマは「矛盾（信号機論）」「断片」「体技心」「華麗な憂うつ」の4本柱、系統は三原康裕（Maison Mihara Yasuhiro）のゆるっとした崩しのシルエット。

## PDFへの変換方法

日本語（Noto Serif JP）と欧文ディスプレイ書体（Cinzel / Cormorant Garamond）のWebフォントを読み込むため、`fonts-local.css` と `fonts/` 以下のフォントファイル一式が必要です（サイズの都合上、本リポジトリには同梱していません）。以下の手順で再生成できます。

```bash
# 1. Google FontsからCSSを取得し、参照されているwoff2を fonts/ にダウンロード
# 2. fonts.googleapis.com のURLをローカルパスに書き換えて fonts-local.css を作成
# 3. Chromiumのヘッドレスモードで印刷

chromium --headless=new --no-sandbox --print-background \
  --print-to-pdf=paradox-wardrobe-concept.pdf \
  --no-pdf-header-footer \
  paradox-wardrobe-concept.html
```

ページサイズは `@page { size: 210mm 297mm; margin: 0; }` でA4フルブリードに設定済みです。
