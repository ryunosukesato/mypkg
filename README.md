# 概要
## ロボットシステム学　課題2のためのリポジトリです
count.pyというノードが1秒間に10ずつ数字が上がり、twice.pyというノードでcount.pyのcount_upから受け取ったデータ（数字）を2倍して出すというプログラムです。

# 動作環境
・Raspberry Pi 4 Model B  
・Ubuntu 20.04  
・ROS noetic

# 環境構築
このパッケージを、以下のようにROSのsrcディレクトリの下にクローンしてください。  
`:~/catkin_ws/src$ git clone （このリポジトリのSSHキー）`

## 環境構築についての補足
このリポジトリをクローンして試してみるべきなのだろうが、既に私のラズパイの中にこのリポジトリと同じものがあるため、環境構築の動作確認は行えていないが、上記のようにROSのsrcディレクトリの下にクローンすれば環境構築はできるはずだ。しかし、以下に示す実行方法は、私のラズパイのディレクトリ（GitHubにpushしたものと同じもの）で動作確認済みである。

# 実行方法
４つの端末が必要です。以下の順に従って、それぞれの端末で実行してください。

1. 端末1でroscoreを実行する  
`$ roscore`

2. 端末2でcount.pyを実行する  
`$ rosrun mypkg count.py`

3. 端末3でtwice.pyを実行する  
`$ rosrun mypkg twice.py`

4. 端末4でデータを取り出す。  
`$ rostopic echo /twice`

### 実行方法についての補足
端末4では端末1,2,3でそれぞれを実行した後、
`$ rostopic list`
と入力することで、今、何のトピックがあるかを確認できます。

# 著者
Ryuichi Ueda　　著者のアカウントのリンクは[こちら](https://github.com/ryuichiueda)

# ライセンス
・BSD 3-Clause "New" or "Revised"

# 参考
このリポジトリの作成時に参考にしたリポジトリは以下の2つです。  
1つ目は[こちら](https://github.com/momokohara/robosys2020_ros)  
2つ目は[こちら](https://github.com/MibuchiYuta/ROS_ServoDriverHAT)
