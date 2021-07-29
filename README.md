# p5.jsで初めてのプログラミング体験
エディターはこちら https://editor.p5js.org/

# まずは円を描いてみましょう。
<img src="images/circle.png" width="600px">

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

