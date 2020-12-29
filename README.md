# robosys2020_kadai1
ロボットシステム学の課題１で作成したプログラムです。

## 概要
講義内で作成したデバイスドライバを一部改造して作成しました。 
0,1,2の入力に応じて1つのLEDが点灯，消灯，10回点滅という3つの動きをします。 

## 動作環境
- Raspberry Pi 4 Model B 
- Ubuntu 20.04 

## 使用したもの
- Raspberry Pi 4 Model B　×1 
- ブレッドボード　×1 
- LED　×1 
- 抵抗 ×1 
- ジャンパーコード（オス-メス）×2 
- ジャンパーコード（オス-オス）×2 

## 回路
下図のように回路を作成しました。　

![kairo](https://user-images.githubusercontent.com/56065468/103296711-fe998f80-4a39-11eb-98c2-017d337bb03d.PNG) 

## 実行手順
以下の手順で実行してください。 

- リポジトリをクローンする  
 
`$ git clone https://github.com/ShioriSugiyama/robosys2020_kadai1.git`  
 
- リポジトリのディレクトリに移動する 
 
`$ cd robosys2020_kadai1` 
 
- 数字の入力ができる状態にする 

`$ make` 

`$ sudo insmod myled.ko` 

`$ sudo chmod 666 /dev/myled0` 

- 終了した際に入力するコマンド 

`$ sudo rmmod myled`

### LEDを点灯させる
`$ echo 0 > /dev/myled0` 

### LEDを消灯させる
`$ echo 1 > /dev/myled0` 

### LEDを10回点滅させる
`$ echo 2 > /dev/myled0` 

## デモ動画

https://youtu.be/RJDrkZwVTqs

## ライセンス
GNU General Public License v3.0
