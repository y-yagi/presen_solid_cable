# Solid Cable on Rails 8.0

* Rails 8.0で新規にアプリケーションを作成した場合、デフォルトでSolid Cableが使われるようになっている

```yml
# cable.yml
production:
  adapter: solid_cable
  connects_to:
    database:
      writing: cable
  polling_interval: 0.1.seconds
  message_retention: 1.day
```
