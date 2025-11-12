# Sample Files Viewer (GitHub Pages)

GitHub Pages で `files/` 配下の PDF / Office ファイルを自動一覧し、別タブで閲覧できるシンプルなサイトです。

## 機能
- **自動一覧**: `files/` に置いた対象ファイルをトップページで自動列挙
- **別タブ表示**:
  - **PDF**: 直接新規タブで開く
  - **Office (Word/Excel/PowerPoint)**: Office Online Viewer で新規タブ表示（doc, docx, xls, xlsx, ppt, pptx）

## セットアップ
1. リポジトリを作成（またはこのフォルダを既存リポジトリに追加）
2. `_config.yml` の公開URL設定をプロジェクトに合わせて修正
   - ユーザーページ（`https://<ユーザー>.github.io`）の場合:
     - `url: "https://<ユーザー>.github.io"`
     - `baseurl: ""`
   - プロジェクトページ（`https://<ユーザー>.github.io/<リポジトリ>`）の場合:
     - `url: "https://<ユーザー>.github.io"`
     - `baseurl: "/<リポジトリ名>"`
3. `files/` に PDF / Office ファイルを配置
4. GitHub に push して、GitHub Pages を有効化
   - GitHub のリポジトリ → Settings → Pages → Source を `main` ブランチ（ルート）に設定
5. 公開URLにアクセスして、一覧と閲覧を確認

## 使い方
- 追加は `files/` フォルダへコピーするだけでOK
- トップ（`index.html`）に自動で表示され、クリックで新規タブを開きます

## 対応拡張子
- PDF: `pdf`
- Office: `doc`, `docx`, `xls`, `xlsx`, `ppt`, `pptx`

## カスタマイズ（拡張子の追加/表示方法の変更）
`index.html` の先頭付近に拡張子の振り分けがあります（PDF/Office など）。ここに拡張子を足すことで対象を広げられます。

例）`office_exts` に `pptx` を含めるなど（既に設定済み）。

## 注意事項
- Office Online Viewer を利用するため、ファイルは「インターネットからアクセス可能」である必要があります（GitHub Pages は公開サイトです）。
- 閲覧対象ファイルに機密情報を含めないでください。
- 大きなファイルは表示に時間がかかる場合があります。

## ローカルプレビュー（任意）
Jekyll をローカルで動かすと、公開前に表示を確認できます（Ruby 環境が必要）。

```bash
# macOS の例（必要に応じて）
gem install bundler jekyll
bundle init
bundle add jekyll
bundle exec jekyll serve
```

起動後、`http://127.0.0.1:4000`（またはコンソールに表示されるURL）にアクセスしてください。

## 構成
- `index.html`: `files/` を自動一覧し、拡張子に応じて閲覧先を切り替え
- `_config.yml`: `url`/`baseurl` など GitHub Pages 用の基本設定
- `files/`: 対象ファイル配置先（`.gitkeep` は空ディレクトリ保持用。不要なら削除可）

## ライセンス
必要に応じて追加してください（例: MIT）。


