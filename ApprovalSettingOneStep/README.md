TeamSpirit 承認プロセス(1段)
==================
<a href="https://githubsfdeploy.herokuapp.com">
  <img alt="Deploy to Salesforce"
       src="https://raw.githubusercontent.com/afawcett/githubsfdeploy/master/src/main/webapp/resources/img/deploy.png">
</a>

説明
--------
TeamSpirit インストールガイドに記載されている下記の承認プロセスを設定します。
- 勤怠申請
- 経費申請
- 事前申請
- 工数実績申請
- 稟議
- 定期区間変更申請

Salesforceボタンを利用する
--------
#### [前提条件]
 - 接続先組織に「TeamSpirit」がインストールされていること

#### Salesforceボタン

1. [Deploy to Salesforce]ボタンをクリックすると、GitHub Salesforce Deploy Toolページが開きます。
1. 右上の[Login to Salesforce]ボタンをクリックすると、ログイン画面に遷移します。但し、ブラウザがすでにSalesforce組織にログインしていた場合、ログイン画面はスキップします。
1. 承認プロセスを設定したいSalesforce組織にログインすると、GitHubリポジトリ情報、デプロイ対象の組織情報、デプロイ対象ファイルが表示されます。
1. 右上の[Deploy]ボタンをクリックすると、承認プロセスのデプロイが開始します。「To Salesforce Org」の下にデプロイ状況が表示されます。「Deployment Complete」と表示されると完了です。

Force.com 移行ツールを利用する
--------

#### [前提条件]
 - Apchage Ant がインストールされており、実行可能なこと
 - Force.com 移行ツール がインストールされており、実行可能なこと
 - 接続先組織に「TeamSpirit」がインストールされていること

#### build.propertiesを利用しない場合
接続先組織のユーザ名、パスワードを環境変数に与えて、Force.com 移行ツールを実行します。

```
$ SF_USERNAME=(User Name) SF_PASSWORD=(Password) ant
```

#### build.propertiesを利用する場合

build.propertiesのSF_USERNAME、SF_PASSWORDに接続先のユーザ名、パスワードを設定し、下記のコマンドを実行します。

```
$ ant
```

ライセンス
--------
Copyright &copy; 2017 TeamSpirit Inc.

[MIT License](http://www.opensource.org/licenses/mit-license.php)

Powered by [GitHub Salesforce Deploy Tool Lightning Edition](https://andyinthecloud.com/2013/09/24/deploy-direct-from-github-to-salesforce/)
