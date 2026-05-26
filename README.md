# レシートCSV変換 PWA

スマホのホーム画面に追加して使えるレシート読み取りアプリです。  
カメラで撮影 → AIが品目を読み取り → CSVにエクスポート

---

## GitHub Pages へのデプロイ手順

### 1. リポジトリを作成

1. GitHub (https://github.com) にログイン
2. 右上の「+」→「New repository」
3. Repository name: `receipt-pwa`（なんでもOK）
4. **Public** を選択（GitHub Pages無料プランはPublic必須）
5. 「Create repository」をクリック

### 2. ファイルをアップロード

表示されたページで「uploading an existing file」をクリックして、  
このZIPを解凍したファイルをすべてドラッグ＆ドロップしてアップロード。

または Git が使える場合：
```bash
git init
git add .
git commit -m "initial commit"
git branch -M main
git remote add origin https://github.com/あなたのユーザー名/receipt-pwa.git
git push -u origin main
```

### 3. GitHub Pages を有効化

1. リポジトリの「Settings」タブ
2. 左メニューの「Pages」
3. Source を「GitHub Actions」に変更
4. 自動でデプロイが始まります（1〜2分）

### 4. URLを確認

`https://あなたのユーザー名.github.io/receipt-pwa/` でアクセスできます。

---

## スマホへのインストール方法

### iPhone (Safari)
1. Safariで上記URLを開く
2. 下の共有ボタン（四角と矢印のアイコン）をタップ
3. 「ホーム画面に追加」をタップ
4. 「追加」をタップ

### Android (Chrome)
1. Chromeで上記URLを開く
2. アドレスバー右の「⋮」→「ホーム画面に追加」
3. または画面下部に表示されるインストールバナーをタップ

---

## 使い方

1. 初回起動時、右上の「APIキー ⚙」をタップ
2. Anthropic APIキー（https://console.anthropic.com/ で取得）を入力して「保存」
3. 「カメラで撮影」または「ライブラリから選択」でレシートを追加
4. 「AI変換を開始」をタップ
5. 結果を「CSVを保存」または「コピー」で取得

APIキーはスマホのローカルストレージに保存されます（他者には共有されません）。
