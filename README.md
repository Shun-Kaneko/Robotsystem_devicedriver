# Robotsystem_devicedriver
ロボットシステム学の演習で作ったデバイスドライバです。
***  
# 実行内容
講義内で作成したデバイスドライバに変更を加えて作成しています。  
  ・1を入力したら、赤のLEDが1回点滅する。  
  ・2を入力したら、黄色のLEDが1回点滅する。  
  ・3を入力したら、青のLEDが1回点滅する。  
  ・4を入力したら、緑のLEDが1点滅する。  
  ・0を入力したら、赤→黄色→青→緑の順で消灯し、その後同じ順に点灯し、その後全てのLEDが1回点滅する。  
   ***
# 使用したもの
  Raspberry Pi 3 ModelB+   
  Breadboard   
  LED ×4(赤×1,黄色×1,青×1,緑×1)   
  抵抗　220Ω ×4   
  Dupont Wire メスーオス ×4   
  Jumper wire ×2  
   ***
# 回路
  LEDをそれぞれアノードが   
  赤→GPIO25   
  黄色→GPIO16   
  青→GPIO20   
  緑→GPIO21   
  に接続している。   
  回路の写真は[こちら](https://user-images.githubusercontent.com/72370478/101281791-937ee380-3814-11eb-90ab-b9b8cb4fdde9.jpeg)です。
  ***
# インストール方法   
インストール手順は下記の通りです。　　
```sh  
git clone http://github/Shun-Kaneko/Robotsystem_devicedriver  
cd Robotsystem_devicedriver/myled  
make  
sudo insmod myled.ko  
sudo chmod 666 /dev/myled0   
```   
***  
# 使用方法   
echo 1 > /dev/myled0　と入力すると赤のLEDが1回点滅する。  
echo 2 > /dev/myled0　と入力すると黄色のLEDが1回点滅する。  
echo 3 > /dev/myled0　と入力すると青のLEDが1回点滅する。  
echo 4 > /dev/myled0　と入力すると緑のLEDが1回点滅する。  
echo 0 > /dev/myled0　と入力すると赤→黄色→青→緑の順で消灯し、その後同じ順に点灯し、その後全てのLEDが1回点滅する。  
***   
# 実行動画
  実行した動画は[こちら](https://www.youtube.com/watch?v=FUy7c3xXVaw)です。  
  ***   
# ライセンス  
[GNU General Public License v3.0](https://github.com/Shun-Kaneko/Robotsystem_devicedriver/blob/main/COPYING)
