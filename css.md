## 要素全体を透明にする
	1.opacity要素

## 属性セレクタについて
### aのhref属性について
	- a[href] -> aのhref属性が存在する場合
	- a[href="foo"] -> href属性がfooという値の場合
	- a[href~="foo"] -> 値がスペース区切りだった時にfooを含む場合
	- a[href^="foo"] -> fooから始まる
	- a[href$="foo"] -> fooで終わる
	- a[href*="foo"] -> fooを含む

## box-shadow / text-shadow
### 四角い領域やテキストに影をつける方法
	- box-shadow // xy座標で指定して、最後に色指定する（ぼかし度合を「.4」などで指定する）
	div {
		width: 200px;
		height: 100px;
		background: #fff;
		box-shadow: 10px 20px 4px 10px rgba(0,0,0,.4) inset, 10px 20px 4px 10px skyblue;
	}
	※ 4つ目の数値で影の大きさを決める、マイナスを指定すると影が小さくなる
	※ insetをつけると影が内側になる
	※ 影は重ねて何個もつけることが出来る

	- text-shadow
	h1 {
		text-shadow:  2px 2px 0 rgba(0,0,0,.4);
	}
	※ 4つ目の数値はつけられない
	※ insetもつけられない

## transform
### transformで要素を変形させてみよう
	- transform -> x方向、y方向の移動距離を指定することができる

	div {
	width: 100px;
	height: 100px;
	margin-bottom: 20px;
	position: absolute;
	top: 100px;
	left: 100px;
	}

	#box1 {
	  background: skyblue;
	  opacity: .5;
	}

	#box2 {
	  background: orange;
	  opacity: .5;
	  /*transform:translate(20px, 40px);*/		// x方向、y方向の移動距離を指定することができる
	  /*transform:translateX(20px);*/			// x方向だけに動く
	  /*transform:scale(0.5, 1.5);*/			// 図形の大きさを変更することができる
	  /*transform:skew(10deg, 20deg);*/			// 傾斜をつける命令 角度をつければOK
	  transform:rotate(30deg);					// 回転効果、時計回りに何度回転させるか
	  /*transform-origin: 50% 50%;*/			// 基点を変える方法 %指定
	  transform-origin: 0 0;					// 基点を変える方法 数値指定
	}



