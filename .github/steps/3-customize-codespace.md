<!--
  <<< Author notes: Step 3 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

## ステップ 3: Codespace をカスタマイズしよう！

_素晴らしい！ :tada: カスタムイメージで Codespace を作成できましたね！_

VS Code の拡張機能を追加したり、機能を追加したり、ホスト要件を設定したりすることで、Codespace をさらにカスタマイズできます。

`devcontainer.json` ファイルでいくつかの設定をカスタマイズしてみましょう！

### :keyboard: アクティビティ: `devcontainer` ファイルにカスタマイズを追加しよう

1. `.devcontainer/devcontainer.json` ファイルに移動します。
1. ファイルの本体で最後の `}` の直前に、以下のカスタマイズを追加します。

   ```jsonc
    ,
    // コンテナ作成時にインストールしたい拡張機能のIDを追加します
    "customizations": {
        "vscode": {
            "extensions": [
                "GitHub.copilot"
            ]
        },
        "codespaces": {
            "openFiles": [
                "codespace.md"
            ]
        }
    }
   ```

1. **Commit changes** をクリックし、**Commit changes directly to the `main` branch** を選択します。
1. リポジトリのトップページに移動し、新しい Codespace を作成します。
1. ページ中央の **Code** ボタンをクリックします。
1. ポップアップで **Codespaces** タブをクリックします。
1. アクティブな Codespace の数が最大（通常は2）に達していないことを確認します。詳細は [Codespace のライフサイクルについて](https://docs.github.com/ja/codespaces/getting-started/understanding-the-codespace-lifecycle) を参照してください。

   > **ヒント**: アクティブな Codespace を停止するには、**<span>&#x25cf;</span>Active** の横の **•••** をクリックし、メニューから **Stop codespace** を選択します。
   
1. **Create codespace on main** ボタンをクリックします。

   > Codespace の起動には約 **2分** かかります。

1. 先ほどと同様に Codespace が起動していることを確認します。
1. VS Code エディタに `codespace.md` ファイルが表示されているはずです。
1. VS Code の拡張機能リストに `copilot` 拡張機能が表示されているはずです。

   これにより、VS Code の拡張機能が追加され、Codespace 起動時にファイルが自動で開かれます。

次に、Codespace 作成時に自動でコードを実行する設定を追加しましょう！

### :keyboard: アクティビティ: Codespace 作成時にコードを実行しよう

1. `.devcontainer/devcontainer.json` ファイルを編集します。
1. ファイルの本体で最後の `}` の直前に、以下の postCreateCommand を追加します。

   ```jsonc
    ,
    "postCreateCommand": "echo '# Writing code upon codespace creation!'  >> codespace.md"
   ```

1. **Commit changes** をクリックし、**Commit changes directly to the `main` branch** を選択します。
1. リポジトリのトップページに移動し、新しい Codespace を作成します。
1. ページ中央の **Code** ボタンをクリックします。
1. ポップアップで **Codespaces** タブをクリックします。
1. **Create codespace on main** ボタンをクリックします。

   > Codespace の起動には約 **2分** かかります。

1. 先ほどと同様に Codespace が起動していることを確認します。
1. `codespace.md` ファイルに `Writing code upon codespace creation!` というテキストが追加されていることを確認します。
1. 約20秒待ってからこのページ（手順を見ているページ）をリロードしてください。[GitHub Actions](https://docs.github.com/ja/actions) により自動的に次のステップに進みます。
