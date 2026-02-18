# Postman入門

## Postmanとは？

**Postman** は、APIにリクエストを送信し、レスポンスを確認できるツールです。  
通常ブラウザでは確認できない：

- POST送信
- ヘッダー情報
- JSONレスポンス確認
- 認証付き通信

などを簡単にテストできます。

---

## Postmanを使う目的

- APIの動作確認
- レスポンスデータの確認
- パラメータのテスト
- 開発中のデバッグ
- バックエンドとの連携確認

👉 API学習・開発現場どちらでもよく利用されるツールです。

---

## 📺導入方法（今回の学習環境）

今回は自分の環境に合わせて説明していきます。  
👉 **VS Code + Postman拡張機能**  
を使用しています。

### ✔メリット

✅VS Code内で完結できる  
✅アプリ版インストール不要  
✅コード編集と同時にテスト可能  

### 導入手順（VS Code）

1. VS Codeを開く
2. 左メニューの「拡張機能」をクリック
3. 検索欄に**Postman**と入力する
4. Installをクリックして、インストールします
5. 必要に応じて再起動を行おう

インストール後、サイドバーにPostmanアイコンが表示されるようになります。

---

## 基本操作の流れの解説

```rust
① URL入力
    ↓
② HTTPメソッド選択
    ↓
③ Sendボタン押下
    ↓
④ レスポンス確認
```

---

## 実際にAPIをたたいてみる

### ▼手順

① 新規リクエスト作成  
② メソッド → `GET`  
③ URL入力：

```arduino
https://jsonplaceholder.typicode.com/users
```

④ Sendをクリック

---

### ▼レスポンス例

```json
[
    {
        "id":1,
        "name":"Leanne Graham",
        "username":"Bret"
    }
]
```

👉サーバーからデータが返ってきた！

---

## クエリパラメータを試す

URLの末尾に条件を付けることで、取得データを絞れます。

### ▼例

```bash
https://jsonplaceholder.typicode.com/users?id=5
```

👉IDが５のユーザー取得

### ▼usernameで検索

```arduino
https://jsonplaceholder.typicode.com/users?username=Antonette
```

👉username一致ユーザー取得

---

## 部分一致検索はできる？

```arduino
https://jsonplaceholder.typicode.com/users?email=.biz
```

結果：

```css
[]
```

👉空配列

### 理由

JSONPlaceholderは：

✅完全一致検索のみの対応  
❌部分一致検索は対応不可

---

## 💡パラメータの仕組み

```ruby
ベースURL
https://jsonplaceholder.typicode.com/users
    +
    ?キー＝値
```

例：

```bash
?id=5
```

👉条件に一致するデータ取得

---

## Postmanで確認できる情報

### Bodyタグ

→JSONレスポンス確認

### Headersタブ

→通信のメタ情報

### Statusタブ

→通信結果

| コード | 意味 |
| ----- | ----- |
| 200 | 成功 |
| 404 | 見つからない |
| 500 | サーバーエラー |

---

## 学習ポイント

Postmanを使うことで：

✅API通信の流れが理解できる  
✅JSONデータ構造に慣れる  
✅フロントとサーバーの関係が理解できる

---

## 次に試してみよう

✔POST送信を残す  
✔BodyにJSONを入れる
✔ヘッダー追加
✔認証付きAPI体験

---

## まとめ

- PostmanはAPIテストツール
- VS Code拡張で簡単に扱うことができる
- GETでデータ取得を体験
- クエリパラメータで検索可能
- APIしようにより部分一致不可の場合アリです

### ひとこと

APIは「触りながら理解する」のが最速だと思いました。  
Postmanはその入り口としては最高のツールでした。

---

👈 前へ → :[10_フロントエンドとAPIの関係](/docs/10_フロントエンドとAPIの関係.md)

👉 次へ → :[99_用語集](/docs/99_用語集.md)

---

👈 TOPへ → :[TOPページ](/README.md)
