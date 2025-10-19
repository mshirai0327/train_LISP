# はじめに

[はじめての Lisp 関数型プログラミング](https://gihyo.jp/book/2016/978-4-7741-8035-9/support)
の勉強ノートです。

## 環境構築

WSL + VScode で構築した
参考：https://zenn.dev/k41531/articles/6a68fa6f1bb08c

wsl 上にディレクトリを作成して、`code .`で VScode を起動する
terminal より、sbcl をインストールする
方法：

```
sudo apt install sbcl
```

(Windows 側でも winget でインストールできるが、パスを通すなど面倒だったので、WSL で完結させた)

Quicklisp をインストール

```
curl -O https://beta.quicklisp.org/quicklisp.lisp
sbcl --load quicklisp.lisp

(補足：ここでlispとの対話型インターフェースが立ち上がる。sbclが正常にインストールできていれば動作する。その後以下を一行ずつ記述してEnterを押下する)

(quicklisp-quickstart:install)
(ql:add-to-init-file)
```

補足：Lisp では、`()`で囲まれたリストによってしょりを記述する。つまり上のコマンドは、Lisp での`pip install`（python で言うなら）的なもの
入力を終えたら、対話インターフェースを閉じる。閉じ方は以下

```
(exit)
```

python で言う、`exit`とか Ctrl + D のようなもの
