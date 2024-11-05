# Solid Cache vs PostgreSQL adapter

* PostgreSQLをadapterとして使っている場合、サイズ制限があった
  * PostgreSQLのPub/Sub(NOTIFY)の制限で8kb
* Solid Cableにはその制限は無い
