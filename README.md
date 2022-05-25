# ElasticSearch
Environment of ElasticSearch with Docker

------------
## 参考
------------
### ElasticSearch kibanaのリファレンス 
https://www.elastic.co/guide/jp/index.html

### 入門
https://dev.classmethod.jp/articles/elasticsearch-starter-1/

------------
## 動作確認
------------
コマンドラインからデータを挿入する場合
- データの挿入
  curl -X POST -H 'Content-Type: application/json' -d @"sample.json" http://localhost:9200/{任意(ドキュメントの名前)}/_doc
- データの取得  
  curl -X GET "http://localhost:9200/{データ挿入時に指定した任意の値}/_doc/(登録したデータのid)"

- データの検索
  curl -X GET "http://localhost:9200/inspection/_search/"

- データの削除
  curle -X DELETE "http://localhost:9200/{データ挿入時に指定した任意の値}/_doc/(登録したデータのid)"

kibanaを使用したデータ挿入
- http://localhost:5601/app/dev_tools#/console