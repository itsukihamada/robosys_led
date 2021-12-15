# robosys_led

 # ロボットシステム学　課題1
  
   0～4の入力したコマンドによって3つのLEDが点灯、消灯、点滅を行う。
    
   講義内で上田先生の作成したデバイスドライバにコードを追加して作成。
    
# 動作環境

  *ubuntu 20.04 server
  
  *Rasberry Pi 4

# 使用したもの
  
  *Rasberry Pi 4
  
  *ブレッドボード
  
  *LED × 3
  
  *抵抗(220Ω) × 3
  
  *ジャンパー線 × 6

# 回路
  
  下記のURLの動画のLEDは右からGPIO25,4,17に接続し、抵抗をGNDとLEDの間に一つずつつないでいる。
  
# インストール方法

  コマンドを入力
  
    git clone git@github.com:itsukihamada/robosys_led.git
    
    cd robosys_led
    
    make
    
    sudo insmod myled.ko
    
    sudo chmod 666 /dev/myled0

# 実行方法

  赤色LEDのみ点灯
  
    echo 1 > /dev/myled0
   
  緑色LEDのみ点灯
   
    echo 2 > /dev/myled0
    
  青色LEDのみ点灯
  
    echo 3 > /dev/myled0
  
  3つのLEDを順番に点灯
  
    echo 4 > /dev/myled0

# 実際の動画

  https://youtu.be/vEeuR3NaynM
    
# ライセンス
  
  COPYING(GNU General Public License v3.0)

  
