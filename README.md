# Robotsystem_devicedriver
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
  回路図は[こちら](https://user-images.githubusercontent.com/72370478/101281791-937ee380-3814-11eb-90ab-b9b8cb4fdde9.jpeg)です。
# 実行方法
実行手順は下記の通りです。　　
'''sh
git clone http://github/Shun-Kaneko/Robotsystem_devicedriver
cd Robotsystem_devicedriver/myled
make
sudo insmod myled.ko
sudo chmod 666 /dev/myled0
echo 1 > /dev/myled0
'''
"1"の部分を2,3,4,0に変えるとそれぞれ動作します。　　
   ***
# 実行動画
  実行した動画は[こちら](https://www.youtube.com/watch?v=FUy7c3xXVaw)です。
