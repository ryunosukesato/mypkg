# このリポジトリは作成途中です
このリポジトリはロボットシステム学　課題2のためのリポジトリです。

# 概要
count.pyというノードが1秒間に10ずつ数字があがり、twice.pyというノードでcount.pyのcount_upから受け取ったデータ（数字）を2倍して出すというプログラムです。

# 動作環境
・Raspberry Pi 4 Model B  
・Ubuntu 20.04  
・ROS noetic

# 環境構築
このパッケージをROSのsrcディレクトリの下にクローンしてください。  
`:~/catkin_ws/src$ git clone （このリポジトリのSSHキー）`

## 環境構築についての補足
このリポジトリをクローンして試してみるべきなのだろうが、既に私のラズパイの中にこのリポジトリと同じものがあるため、環境構築の動作確認は行えていないが、上記のようにROSのsrcディレクトリの下にクローンすれば環境構築はできるはずだ。しかし、以下に示す実行方法は、私のラズパイのディレクトリ（GitHubにpushしたものと同じもの）で動作確認済みである。

# 実行方法
４つの端末が必要です。以下の順に従って、それぞれの端末で実行してください。
## 端末1
`$ roscore`

## 端末2
`$ rosrun mypkg count.py`

## 端末3
`$ rosrun mypkg twice.py`

## 端末4
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
