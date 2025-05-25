<!--
  <<< Author notes: Step 2 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

## ステップ 2: Codespace にカスタムイメージを追加しよう！

_素晴らしい！ :tada: 最初の Codespace を作成し、VS Code でコードをプッシュできましたね！_

リポジトリの開発コンテナを設定することで、そのリポジトリで作成されるすべての Codespace に、プロジェクトに必要なツールやランタイムが揃った最適な開発環境を提供できます。

**開発コンテナ（dev container）とは？**  
開発コンテナ（dev container）は、完全な開発環境を提供するよう特別に構成された Docker コンテナです。Codespace で作業するたびに、仮想マシン上の dev container を利用しています。

dev container ファイルは JSON 形式で、Codespace で動作するデフォルトイメージや VS Code の設定、カスタムコードの実行、ポートのフォワードなどをカスタマイズできます。

それでは、`devcontainer.json` ファイルを追加してカスタムイメージを指定しましょう。

### :keyboard: アクティビティ: .devcontainer.json ファイルを追加して Codespace をカスタマイズしよう

1. リポジトリの **Code** タブに戻り、**Add file** ドロップダウンボタンをクリックし、`Create new file` を選択します。
1. ファイル名入力欄に、次の内容を入力または貼り付けます。

   ```
   .devcontainer/devcontainer.json
   ```

1. 新しい **.devcontainer/devcontainer.json** ファイルの本文に、次の内容を追加します。

   ```jsonc
   {
     // この構成の名前
     "name": "Codespace for Skills!",
     // ベースとなる codespace イメージを使用
     "image": "mcr.microsoft.com/vscode/devcontainers/universal:latest",

     "remoteUser": "codespace",
     "overrideCommand": false
   }
   ```

1. **Commit changes** をクリックし、**Commit changes directly to the `main` branch** を選択します。
1. リポジトリの **Code** タブに戻り、新しい Codespace を作成します。
1. ページ中央の緑色の **Code** ボタンをクリックします。
1. ポップアップで **Codespaces** タブをクリックします。
1. **Create codespace on main** ボタン、またはタブの `+` アイコンをクリックします。これで main ブランチ上に新しい Codespace が作成されます。（他の Codespace もここに表示されます）

   > Codespace の起動には約 **2分** かかります。

1. 先ほどと同様に、新しい Codespace が起動していることを確認します。

   使用されているイメージは GitHub Codespaces で提供されるデフォルトイメージです。Python、Node.js、Docker などのランタイムやツールが含まれています。全リストはこちら: https://aka.ms/ghcs-default-image  
   開発チームは必要な前提条件がインストールされた任意のカスタムイメージを利用できます。詳細は [codespace image](https://aka.ms/configure-codespace) を参照してください。

1. 約20秒待ってからこのページ（手順を見ているページ）をリロードしてください。[GitHub Actions](https://docs.github.com/ja/actions) により自動的に次のステップに進みます。
