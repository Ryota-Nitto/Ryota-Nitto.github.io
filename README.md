# Ryota NITTO Portfolio Site

日塔諒太（Ryota NITTO）のポートフォリオサイトです。GitHub Pagesで公開する静的サイトとして構成しており、トップページにプロフィール、研究業績、社会実装、学歴、スキル、職歴をまとめ、各プロジェクトの詳細ページへ遷移できます。

公開URL: https://nittoryota.com/

## サイト仕様

- 日本語 / 英語の表示切り替えに対応
- トップページは左サイドバー + メインコンテンツの2カラム構成
- モバイル幅では1カラムに切り替わるレスポンシブレイアウト
- Lucide IconsをCDNから読み込み、セクション見出しや連絡先に使用
- OGP / Twitter Card / canonical / JSON-LDを設定
- カスタムドメインは`CNAME`で`nittoryota.com`を指定
- フレームワークやビルド工程を使わないHTML / CSS / JavaScriptのみの静的実装

## 掲載コンテンツ

トップページ（`index.html`）には以下を掲載しています。

- プロフィール・所属・連絡先
- Mission
- Creative Projects
- Research Publications
- Social Implementation
- Education
- Skills
- Fellowship
- Work Experience

## プロジェクトページ

`projects/`配下に個別ページを配置しています。

- `dynadrink.html`: DynaDrink
- `utsuroi-drink.html`: うつろいドリンク
- `beatim-runner.html`: Beatim Runner
- `walking-drummer.html`: Walking Drummer
- `suikuu.html`: 大阪万博 高原レストラン 水空
- `watapa.html`: わたぱ！
- `plarailers.html`: プラレーラーズ
- `beatim.html`: `beatim-runner.html`へのリダイレクトページ

## ディレクトリ構成

```text
.
├── CNAME
├── README.md
├── index.html
├── style.css
├── images/
│   ├── DynaDrink.png
│   ├── beatim-runner.png
│   ├── beatim.png
│   ├── face.jpeg
│   ├── plarailers.jpeg
│   ├── suikuu.jpeg
│   ├── suikuu.jpg
│   ├── utsuroi-drink.png
│   ├── walking-drummer.png
│   └── watapa.png
└── projects/
    ├── beatim-runner.html
    ├── beatim.html
    ├── dynadrink.html
    ├── plarailers.html
    ├── style.css
    ├── suikuu.html
    ├── utsuroi-drink.html
    ├── walking-drummer.html
    └── watapa.html
```

## 技術構成

- HTML: ページ構造、SEOメタ情報、日英テキスト
- CSS: ダークテーマ、カードUI、レスポンシブレイアウト
- JavaScript: 言語切り替え、URLクエリ反映、Lucide Icons初期化
- Assets: `images/`内のプロフィール画像・プロジェクト画像

トップページの言語切り替えは`?lang=ja` / `?lang=en`をURLに反映します。プロジェクト詳細ページでは、選択言語を`localStorage`に保存します。

## ローカル確認

ビルドは不要です。ブラウザで`index.html`を直接開くか、簡易サーバーで確認できます。

```bash
python3 -m http.server 8000
```

起動後、以下にアクセスします。

```text
http://localhost:8000/
```

## 更新方法

- トップページの掲載内容を更新する場合は`index.html`を編集
- 全体の見た目を変更する場合は`style.css`を編集
- プロジェクト詳細ページを更新する場合は`projects/*.html`を編集
- プロジェクト詳細ページ共通の見た目を変更する場合は`projects/style.css`を編集
- 画像を差し替える場合は`images/`へ配置し、HTML側の`src`を更新

## デプロイ

`main`ブランチへpushすると、GitHub Pagesの設定に従って公開されます。独自ドメインは`CNAME`で管理しています。
