# モグラたたきゲーム

![モグラたたきゲーム](mole.gif)

## フォルダ階層

```
mole
├── index.html
├── script.js
└── style.css
```

## HTMLファイルの構造


```html
<body>
    <h1>モグラたたきゲーム</h1>
    <h2>スコア：<span class="score">0</span></h2>
    <p><button>Start!</button></p>

    <div class="game">
      <div class="hole hole1">
        <div class="mole"></div>
      </div>
      <div class="hole hole2">
        <div class="mole"></div>
      </div>
      <div class="hole hole3">
        <div class="mole"></div>
      </div>
      <div class="hole hole4">
        <div class="mole"></div>
      </div>
      <div class="hole hole5">
        <div class="mole"></div>
      </div>
      <div class="hole hole6">
        <div class="mole"></div>
      </div>
    </div>

    <script src="script.js"></script>
  </body>
```


## プログラムの流れ


1. Start!ボタンをクリック
2. 10秒のカウント開始
3. ランダムでどこか一つの穴からモグラを表示させ、1秒たったら非表示に
4. モグラが表示されている間に、モグラをクリックしたらスコアを加算し表示
5. 10秒のカウントが残っていれば 3に戻り実行
6. 10秒のカウントが終了していれば 3の実行を終了しアラートで結果表示


## 使用するメソッドやプロパティ


使用する主なメソッドやプロパティを記述します。
適宜リサーチしながら使用します。

|メソッド名|用途|
|:--|:--|
|querySelector()|スコア(.score)やボタン(button)要素取得|
|querySelectorAll()|穴(.hole)やモグラ(.mole)要素取得|
|addEventListener()　又は onClick()|Start!ボタンがクリックされた時のゲーム開始とモグラがクリックされた時のスコア加算|
|textContent|スコアの表示|
|style.visibility|ボタンの表示・非表示|
|classList.add()|特定の要素に引数のクラス名を追加する。モグラの表示時に使用|
|classList.remove()|特定の要素に引数のクラス名があればそのクラス名を削除する。モグラの非表示時に使用|
|Math.random()|ランダム値を生成|
|Math.floor()|値を丸める|
|setTimeout()|ゲーム開始から10秒間のカウントとモグラ表示非表示の1秒間のカウント|


## ヒント


このスクリプトで難しい部分は、ゲーム時間である10秒間のカウントをしている間に、モグラの表示から非表示までの1秒カウントも同時にする必要があることです。

これに関してはsetTimeout()の非同期関数の動作について確認する必要がありますので、下記のMDNを参考にしてください。

[setTImeout - 非同期関数の動作](https://developer.mozilla.org/ja/docs/Web/API/setTimeout#%E9%9D%9E%E5%90%8C%E6%9C%9F%E9%96%A2%E6%95%B0%E3%81%AE%E5%8B%95%E4%BD%9C)
