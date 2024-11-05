# Solid Cable on Rails 8.0

* テーブルを追加するためのmigrationファイルではなく、専用のschemaファイルが生成される

```ruby
# cache_schema.rb
ActiveRecord::Schema[7.1].define(version: 1) do
  create_table "solid_cable_messages", force: :cascade do |t|
    t.binary "channel", limit: 1024, null: false
    t.binary "payload", limit: 536870912, null: false
    t.datetime "created_at", null: false
    t.integer "channel_hash", limit: 8, null: false
    t.index ["channel"], name: "index_solid_cable_messages_on_channel"
    t.index ["channel_hash"], name: "index_solid_cable_messages_on_channel_hash"
    t.index ["created_at"], name: "index_solid_cable_messages_on_created_at"
  end
end
```

* 通常のアプリケーションとは別のDBで扱う想定
* 通常のアプリケーションと同じDBにしたい場合、上記schemaはmigrationファイルに移動するなどの手作業が必要
