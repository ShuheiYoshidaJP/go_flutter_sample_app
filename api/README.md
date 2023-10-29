# サーバーサイドの要件

## 使用技術:

* Go
* GraphQL
* PostgreSQL

## データ構造:

ユーザー(User)には以下のフィールドが含まれます。

- ID (int): プライマリーキー
- Name (string): ユーザーの名前
- Email (string): ユーザーのメールアドレス
- Age (int): ユーザーの年齢
- Bio (string, optional): ユーザーの簡単な紹介

## エンドポイント:

### Query:

- getUser(id: Int!): User: 指定されたIDのユーザー情報を取得します。
- listUsers: [User]: すべてのユーザー情報をリストとして取得します。

### Mutation:

- addUser(name: String!, email: String!, age: Int!, bio: String): User: 新しいユーザーをデータベースに追加します。
- updateUser(id: Int!, name: String, email: String, age: Int, bio: String): User: 指定されたIDのユーザー情報を更新します。
- deleteUser(id: Int!): Boolean: 指定されたIDのユーザーをデータベースから削除します。

## データベース:

PostgreSQLを使用してください。ユーザーの情報を保存するためのテーブルを設計し、必要なカラムを追加してください。

## サーバー起動:

サーバーはlocalhost:8080で起動し、GraphQLのエンドポイントとして/graphqlを提供してください。

## 参考サイト:

[Goで学ぶGraphQLサーバーサイド入門](https://zenn.dev/hsaki/books/golang-graphql)
