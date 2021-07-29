# p5.jsで初めてのプログラミング体験
エディターはこちら https://editor.p5js.org/
<br>
<br>

## まずは円を描いてみましょう。
<img src="images/circle.png" width="800px">

```
function setup() {
  // キャンバスのサイズ
  createCanvas(400, 400);
}

function draw() {
  
  // 背景色 0は黒
  background(0);
  
  fill(255,255,0);
  
  // x座標 y座標 円の直径
  circle(200,200,100);
}
```
<br>
<br>

## マウスを使ったインタラクティブな表現

<img src="images/mouse.png" width="800px">

```
function setup() {
  // キャンバスのサイズ
  createCanvas(400, 400);
  
  // 背景黒に
  background(0);
  
}

function draw() {
  
  //ランダムな色に
  fill(random(255),random(255),random(255));
  
  // x座標 y座標 円の直径
  circle(mouseX, mouseY,50);
}
```

### setupとdrawについて
p5.jsでは、最初の一回だけ実行したい処理をsetup()内に、常時繰り返し実行したい処理をdraw()内に記述します。<br>
（サイズや背景設定などはsetup()内に、描画部分はdraw()に記述するのが流儀です。）<br>
drawは1秒間に60回実行されます。

<br>
<br>

## 変数を使ったアニメーション
変数とは値をいれる箱のこと。ひとまず「pcのフォルダにデータを入れる、上書き保存も可能」というような理解でOKです。<br>
C言語やJavaScript、ほぼ全てのプログラム言語で利用する重要な概念です。


<img src="images/let.png" width="800px">

```

// 変数の宣言
// let 変数名 = 値;

let posX = 100;

function setup(){
  createCanvas(400,400);
}

function draw(){
  // 白で再度塗りつぶす
  background(255,255,255);
  
  // 青色に
  fill(0,0,255);
  
  // posXの場所に円描く
  circle(posX,200,50);
  
  // posXの値の更新
  posX = posX + 2;
}

```

<br>
<br>

## アニメーションにif文を使ってみる
if文は「もし〜だったらこういう処理をする」といったように使用する条件分岐に使う命令分です。

```

// 変数の宣言
// let 変数名 = 値;

let posX = 100;

function setup(){
  createCanvas(400,400);
  
}

function draw(){
  
  // 白で再度塗りつぶす
  background(255,255,255);
  
  // 青色に
  fill(0,0,255);
  
  // posXの場所に円描く
  circle(posX,200,50);
  
  // posXの値の更新
  posX = posX + 2;
  
  // posXの値が400を超えたら再度0に戻す
  if(posX > 400){
    posX = 0;
  }
  
}

```

<br>
<br>

## よりジェネラティブな表現に挑戦してみよう！
今までの知識と、三角形を描く命令、triangle()を使って、すりガラスのような表現を作ってみましょう。<br>
（少し難しいかも）<br>

<img src="traiangle.png" width="600px">

```
triangle(1番目の点のx座標, 1番目の点のy座標, 2番目の点のx座標, 2番目の点のy座標, 3番目の点のx座標, 3番目の点のy座標);

例: triangle(100,100, 100,200, 200, 100);
```


```
function setup(){
  createCanvas(1000,1000);
  background(0);
  
  // 図形の周りの線を無し
  noStroke();
}

function draw(){
  
  // ランダムな色、透明度に
  fill(random(255),random(255),random(255),random(255));
  
  // 三角形の頂点1
  let x1 = mouseX + random(-100,100);
  let y1 = mouseY + random(-100,100);
  
  // 三角形の頂点2
  let x2 = mouseX + random(-100,100);
  let y2 = mouseY + random(-100,100);
  
  // 三角形の頂点3
  let x3 = mouseX + random(-100,100);
  let y3 = mouseY + random(-100,100);
  
  // 三角形の描画
  triangle(x1,y1,x2,y2,x3,y3);
}
```





### 色の指定方法
fill();のカッコの中に0~255の3つの数字を入れる。
<br>
<img src="images/colors.png" width="600px">

```
例 

赤 fill(255,0,0);
緑 fill(0,255,0);
青 fill(0,0,255);

黄色fill(255,255,0);

```
