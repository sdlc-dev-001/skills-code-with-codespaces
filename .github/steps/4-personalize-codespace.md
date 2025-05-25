<!--
  <<< Author notes: Step 4 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

## ステップ 4: Codespace をパーソナライズしよう！

_Codespace のカスタマイズ、お疲れさまでした！_ :partying_face:

どんな開発環境でも、自分の好みやワークフローに合わせて設定やツールをカスタマイズすることは重要です。GitHub Codespaces では、Codespace をパーソナライズする主な方法が2つあります：VS Code の `Settings Sync` と `dotfiles` です。

このアクティビティでは `dotfiles` に注目します。

**`dotfiles` とは？**  
dotfiles とは、Unix系システムで「.」から始まるファイルやフォルダのことで、アプリケーションやシェルの設定を管理します。これらの dotfiles を GitHub のリポジトリで管理できます。

実際にやってみましょう！

### :keyboard: アクティビティ: Codespace で `dotfile` を有効にしよう

1. リポジトリのトップページから始めます。
1. 画面右上のプロフィール写真をクリックし、**Settings** をクリックします。
1. サイドバーの **Code, planning, and automation** セクションで **Codespaces** をクリックします。
1. **Dotfiles** の項目で **Automatically install dotfiles** を選択し、GitHub Codespaces が新しい Codespace 作成時に自動で dotfiles をインストールするようにします。
1. **Select repository** をクリックし、現在作業中のリポジトリを dotfiles のリポジトリとして選択します。

### :keyboard: アクティビティ: リポジトリに `dotfile` を追加して Codespace を実行しよう

1. リポジトリのトップページから始めます。
1. ページ中央の **Code** ボタンをクリックします。
1. ポップアップで **Codespaces** タブをクリックします。
1. **Create codespace on main** ボタンをクリックします。

   > Codespace の起動には約 **2分** かかります。

1. Codespace が起動していることを確認します。ブラウザには VS Code のウェブエディタとターミナルが表示されているはずです。

   ![codespace1](https://user-images.githubusercontent.com/26442605/207355196-71aab43f-35a9-495b-bcfe-bf3773c2f1b3.png)

1. Codespace 内の VS Code エクスプローラーで新しいファイル `setup.sh` を作成します。
1. ファイルに次のコードを入力します。

   ```bash
   #!/bin/bash

   sudo apt-get update
   sudo apt-get install sl
   echo "export PATH=\$PATH:/usr/games" >> ~/.bashrc
   ```

1. ファイルを保存します。  
   > **注**: ファイルは自動保存されるはずです。
1. ファイルの変更をコミットします。VS Code のターミナルで次を入力：

   ```shell
   git add setup.sh --chmod=+x
   git commit -m "Adding setup.sh from the codespace!"
   ```

1. 変更をリポジトリにプッシュします。VS Code のターミナルで次を入力：

   ```shell
   git push
   ```

1. リポジトリのホームページに戻り、`setup.sh` が正しくプッシュされたことを確認します。
1. Codespace のブラウザタブを閉じます。
1. **Create codespace on main** ボタンをクリックします。

   > Codespace の起動には約 **2分** かかります。

1. 先ほどと同様に Codespace が起動していることを確認します。
1. VS Code エディタに `setup.sh` ファイルが存在することを確認します。
1. VS Code のターミナルで次を入力または貼り付けます。

   ```shell
   sl
   ```

1. アニメーションを楽しみましょう！
1. 約20秒待ってからこのページ（手順を見ているページ）をリロードしてください。[GitHub Actions](https://docs.github.com/ja/actions) により自動的に次のステップに進みます。
