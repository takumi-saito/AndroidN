##### Android N
1. Multi-Window Support
    「マルチウィンドウ」は、アプリを起動している状態でタスクキーを長押しするか、アプリ一覧画面でアプリのサムネイルを長押し後、ドラッグ＆ドロップすることで利用できる
    マルチウィンドウ用のライフサイクルがある

- Notifications
  通知領域のメッセージカードの幅が広がり視認性の向上
  メッセージカードにアプリの通知設定を表示
  ハングアウトなどのアプリでメッセージを受信すると、その場で返信・アーカイブ・再通知することができる
    返信を選択した場合、入力ボックスが現れそのまま返信することができる
  通知領域の最上部に各機能のON/OFFトグル機能を持つようになる

- Data Saver（データ セーバー）
  モバイル通信量を抑えるための機能。
  有効化されていると、WI-FI接続時以外はバックグラウンドのデータ通信の利用ができなくなる。

  ```java
  ConnectivityManager connMgr = (ConnectivityManager)
          getSystemService(Context.CONNECTIVITY_SERVICE);
  // Checks if the device is on a metered network
  if (connMgr.isActiveNetworkMetered()) {
    // Checks user’s Data Saver settings.
    switch (connMgr.getRestrictBackgroundStatus) {
      case RESTRICT_BACKGROUND_STATUS_ENABLED:
      // データセーバー有効状態

      case RESTRICT_BACKGROUND_STATUS_WHITELISTED:
      // アプリがホワイトリストに登録されている
      // フォアグラウンド、バックグラウンドにてより少ないデータを使用する必要がある

      case RESTRICT_BACKGROUND_STATUS_DISABLED:
      // データセーバ無効状態

    }
  } else {
    // データ通信が利用できない状態
  }
  ```

- TV Recording

- Network Security Configuration

- ICU4J Android Framework APIs

- Java 8 Language Features
  JDK1.8に対応
  正し、以下の環境であること
  Android Studio 2.1 (preview)
  Android N Preview
  SDK環境があること
  Android for Work Updates
