# Service

- RPCメソッドの実装単位
  - サービス内に定義するメソッドがエンドポイントになる
  - 1サービス内に複数のメソッドを定義できる
- サービス名、メソッド名、引数、戻り値を定義する必要がある
- コンパイルしてgoファイルに変換するとインターフェースになる
  - アプリケーション側でこのインターフェースを実装する
  ```
  message SayHelloRequest {}
  message SayHelloResponse {}

  service Greeter {
    rpc SayHello (SayHelloRequest) returns (SayHelloResponse);
  }
  ```