# Extensions Manifest Checker

2024年6月にGoogle Chromeは、開発者向けのバージョン（Dev、Canary、Beta）でManifest V2の拡張機能を無効化し、ChromeウェブストアからのManifest V2拡張機能のインストールを不可能にします。  
また、インストールされているManifest V2 拡張機能が自動的に無効化されます。  
この変更は段階的に進められ、ユーザーと開発者からのフィードバックをもとに調整が行われます。
安定版(Stableチャンネル)へのロールアウトは、少なくとも1か月の観察期間を経て、具体的な時期は収集したデータに基づき決定され、段階的に行われます。  
Microsoft Edgeも、Google Chromeの変更に追随し、同様のスケジュールでManifest V2の拡張機能を無効化すると思われます。

Manifest V2の拡張機能を使用している場合は、Manifest V3の類似の拡張機能に移行する必要があります。

このツールでは、利用の環境でどの程度の拡張機能が影響を受けるかを確認できます。

参考: [Manifest V2 のサポート タイムライン](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline?hl=ja)

## インストール方法

### Windows
[ここ](../../raw/main/windows/Extensions%20Manifest%20Checker.exe)からダウンロードして実行してください。

### macOS
[ここ](../../raw/main/macos/Extensions%20Manifest%20Checker_1.4.0_x64.dmg)からdmgをダウンロードし、アプリケーションディレクトリにアプリをコピーしてください。  
アプリは署名されていないので、初めて起動する際にはセキュリティ設定を変更する必要があります。  
初回は `Extensions Manifest Checker` を実行後、
OSの `システム設定` => `プライバシーとセキュリティ` => `セキュリティ` => `このまま開く` で起動してください。

## 使い方

起動すると、Chromeのデフォルトディレクトリを読み取り、拡張機能を一覧表示します。  
本アプリでは、リミットを2024年6月+1か月としています。

![スクリーンショット-2024-03-11-23-43-05](https://github.com/owayo/extensions_manifest_checker/assets/20108042/afc3bd06-c5f3-4607-a924-1e7daf100261)

デフォルトのディレクトリ以外を選択する場合は、`EXTENSIONS ディレクトリ選択`ボタンをクリックし、プロファイル配下の`Extensions`ディレクトリを選択してください。

拡張のインストール/アンインストールを行い、`更新`ボタンをクリックすると、変更が反映されます。
