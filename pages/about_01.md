# Solid Cable

* [https://github.com/rails/solid_cable](https://github.com/rails/solid_cable)
* Action Cableのadapterで、Railsが公式でサポートしている全てのRDBMSをAction Cableのバックエンドとして使用出来るようにしたライブラリ
* 元々バックエンドで使えるのはRedis、PostgreSQLのみで、MySQL、SQLiteは使えなかった
    * Action CableがPub/Subを使う事を前提としており、Pub/Subがサポートされいえるのが上記のみだった為
