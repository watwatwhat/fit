# Karamo Policy Pages

このリポジトリは、Karamoアプリケーションの利用規約とプライバシーポリシーをGitHub Pagesで公開するためのものです。

## 📋 公開されているページ

- **メインページ**: https://watwatlab.github.io/fittrack-policy/
- **利用規約**: https://watwatlab.github.io/fittrack-policy/termsOfUse/
- **プライバシーポリシー**: https://watwatlab.github.io/fittrack-policy/privacy/

## 🚀 セットアップ手順

### 1. リポジトリの作成
```bash
# 新しいリポジトリを作成
git init
git add .
git commit -m "Initial commit: Add terms of use and privacy policy"
git branch -M main
git remote add origin https://github.com/watwatlab/fittrack-policy.git
git push -u origin main
```

### 2. GitHub Pagesの有効化
1. GitHubリポジトリの「Settings」タブに移動
2. 左サイドバーの「Pages」をクリック
3. 「Source」で「GitHub Actions」を選択
4. ワークフローが自動的に実行され、サイトがデプロイされます

### 3. カスタムドメインの設定（オプション）
独自ドメインを使用する場合：
1. `CNAME` ファイルをルートディレクトリに作成
2. ドメイン名を記載（例：`policy.watwatlab.com`）
3. DNS設定でCNAMEレコードを設定

## 📁 ファイル構造

```
policy/
├── index.html              # メインページ
├── termsOfUse/
│   └── index.html          # 利用規約
├── privacy/
│   └── index.html          # プライバシーポリシー
├── _config.yml             # Jekyll設定
├── Gemfile                 # Ruby依存関係
├── .github/
│   └── workflows/
│       └── pages.yml       # GitHub Actionsワークフロー
└── README.md               # このファイル
```

## 🔧 ローカル開発

### 前提条件
- Ruby 3.1以上
- Bundler

### セットアップ
```bash
# 依存関係のインストール
bundle install

# ローカルサーバーの起動
bundle exec jekyll serve

# ブラウザで http://localhost:4000 にアクセス
```

## 📝 コンテンツの更新

### 利用規約の更新
1. `termsOfUse/index.html` を編集
2. 「最終更新日」を現在の日付に変更
3. 変更をコミット・プッシュ

### プライバシーポリシーの更新
1. `privacy/index.html` を編集
2. 「最終更新日」を現在の日付に変更
3. 変更をコミット・プッシュ

## 🔄 自動デプロイ

GitHub Actionsワークフローにより、`main`ブランチへのプッシュ時に自動的にサイトがデプロイされます。

### ワークフローの流れ
1. コードのチェックアウト
2. Ruby環境のセットアップ
3. Jekyll依存関係のインストール
4. サイトのビルド
5. GitHub Pagesへのデプロイ

## 📱 アプリとの連携

Karamoアプリの設定画面から以下のURLにアクセスできます：

```dart
// 利用規約
Navigator.of(context).push(
  MaterialPageRoute(
    builder: (context) => const WebViewPage(
      title: '利用規約',
      url: 'https://watwatlab.github.io/fittrack-policy/termsOfUse/',
    ),
  ),
);

// プライバシーポリシー
Navigator.of(context).push(
  MaterialPageRoute(
    builder: (context) => const WebViewPage(
      title: 'プライバシーポリシー',
      url: 'https://watwatlab.github.io/fittrack-policy/privacy/',
    ),
  ),
);
```

## 🛡️ セキュリティ

- すべてのページはHTTPS経由で配信されます
- GitHub Pagesの標準的なセキュリティ機能が適用されます
- 個人情報は収集されません（静的サイトのため）

## 📞 お問い合わせ

ポリシーに関するご質問は以下までご連絡ください：

- **一般お問い合わせ**: support@watwatlab.com
- **プライバシー関連**: privacy@watwatlab.com
- **データ保護責任者**: dpo@watwatlab.com

## 📄 ライセンス

このプロジェクトのコンテンツは著作権により保護されています。
利用規約とプライバシーポリシーの内容は、watwatlabが所有しています。 