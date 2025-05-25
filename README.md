<header>

<!--
  <<< Author notes: Course header >>>
  Read <https://skills.github.com/quickstart> for more information about how to build courses using this template.
  Include a 1280×640 image, course name in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Next to "About", add description & tags; disable releases, packages, & environments.
  Add your open source license, GitHub uses the MIT license.
-->

# GitHub Codespaces と Visual Studio Code でコードを書く

_GitHub Codespaces と Visual Studio Code を使って開発しよう！_

</header>

<!--
  <<< Author notes: Step 1 >>>
  Choose 3-5 steps for your course.
  The first step is always the hardest, so pick something easy!
  Link to docs.github.com for further explanations.
  Encourage users to open new tabs for steps!
-->

## ステップ 1: 最初の Codespace を作成してコードをプッシュしよう

_「GitHub Codespaces と Visual Studio Code で開発しよう」へようこそ！ :wave:_

**ソフトウェア開発で Codespace を使うことの大きなメリットは何でしょうか？**  
Codespace はクラウド上でホストされる開発環境です。プロジェクトに設定ファイルをコミットすることで（これを構成管理とも呼びます）、すべてのユーザーが同じ Codespace 構成を再現できるようになります。作成した各 Codespace は、GitHub によって Docker コンテナ内の仮想マシン上でホストされます。必要なリソースに応じてマシンタイプを選択できます。

GitHub には、開発チームが Codespace をカスタマイズし、最適な構成やパフォーマンスを実現するためのさまざまな機能があります。たとえば、以下のことができます：

- リポジトリから Codespace を作成する
- Codespace からリポジトリへコードをプッシュする
- VS Code でコードを開発する
- カスタムイメージで Codespace をカスタマイズする
- Codespace を管理する

GitHub Codespaces を使った開発を始めるには、テンプレートや任意のブランチ・コミットから Codespace を作成できます。テンプレートから作成する場合は、空のテンプレートや用途に合ったテンプレートを選べます。

### :keyboard: アクティビティ: Codespace を起動しよう

**これからの作業は別のブラウザタブで進めることをおすすめします。この手順を参照しやすくなります。**

1. リポジトリのトップページを開きます。
1. ページ中央にある緑色の **Code** ボタンをクリックします。
1. ポップアップで **Codespaces** タブを選択し、**Create codespace on main** ボタンをクリックします。

   > Codespace の起動には約2分かかります。  
   > **注**: バックグラウンドで仮想マシンが起動しています。

1. Codespace が起動したことを確認します。ブラウザには VS Code のウェブエディタとターミナルが表示されているはずです。例：
   ![codespace1](https://user-images.githubusercontent.com/26442605/207355196-71aab43f-35a9-495b-bcfe-bf3773c2f1b3.png)

### :keyboard: アクティビティ: Codespace からリポジトリへコードをプッシュしよう

1. Codespace 内の VS Code エクスプローラーで `index.html` ファイルを選択します。
1. **h1** ヘッダーを以下の内容に置き換えます：

   ```html
   <h1>Hello from the codespace!</h1>
   ```

1. ファイルを保存します。  
   > **注**: ファイルは自動保存されるはずです。
1. VS Code のターミナルで、次のコミットメッセージを入力してファイルの変更をコミットします：

   ```shell
   git commit -a -m "Adding hello from the codespace!"
   ```

1. 変更をリポジトリにプッシュします。VS Code のターミナルで次を入力：

   ```shell
   git push
   ```

1. これでコードがリポジトリにプッシュされました！
1. リポジトリのホームページに戻り、`index.html` を開いて新しいコードが反映されていることを確認します。
1. 約20秒待ってからこのページ（手順を見ているページ）をリロードしてください。[GitHub Actions](https://docs.github.com/ja/actions) により自動的に次のステップに進みます。

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

サポート: [ディスカッションボードで質問](https://github.com/orgs/skills/discussions/categories/code-with-codespaces) &bull; [GitHub ステータスページ](https://www.githubstatus.com/)

&copy; 2023 GitHub &bull; [行動規範](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT ライセンス](https://gh.io/mit)

</footer>
