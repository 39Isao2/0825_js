# p5.jsで初めてのプログラミング体験
エディターはこちら https://editor.p5js.org/

## まずは円を描いてみましょう。
<img src="images/circle.png" width="800px">
<br>
### ソースコードはこちら
<br>

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
