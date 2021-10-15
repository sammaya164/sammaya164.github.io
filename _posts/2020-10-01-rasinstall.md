---
categories: "ラズパイ"
title: "#01_Raspberry Pi OSをインストールする"
---

## インストール手順
1. 「Raspberry Pi Imager」をPCにインストールする
   * [Raspberry Piの公式サイト](https://www.raspberrypi.org/downloads/)を開く
   * インストーラをダウンロードする  
     (Windowsの場合なら`Download for Windows`をクリック)
   * ダウンロードしたファイルを実行する 
1. 「Raspberry Pi Imager」を起動する
1. `CHOOSE OS` をクリックして`Raspberry Pi OS (32bit)`を選択する
   `Raspberry Pi OS (Other)`から`Raspberry Pi OS Full(32bit)`を選択しても良い
1. MicroSDカード(16GB以上推奨)をPCに接続する
1. `CHOOSE SD CARD`をクリックして、インストール先のMicroSDカードを選択する
1. `WRITE`をクリックして、書き込みが始まる。20分くらい待つ
1. 書き込みが完了したら、`CONTINUE`をクリックし、MicroSDカードを取り外す
1. MicroSDカードをRaspberry Piに取り付ける
1. Raspberry Piにモニター、キーボード、マウスを接続する
1. Raspberry Piを電源につないで起動する
1. 「Welcome to Raspberry Pi」のウィンドウが表示されたら`Next`をクリック
1. Set Country
   * Country: Japanを選択する
   * Language: Japaneseを選択する
   * Timezone: Tokyoを選択する
   * `Next`をクリック
1. Change Password
   * パスワードを設定する
   * `Next`をクリック
1. Set Up Screen
   * デスクトップ画面の周囲が黒く見えている場合は`This screen shows a black border around desktop`にチェックを入れる
   * `Next`をクリック
1. Select WiFi Network
   * `Skip`をクリック  
     (ここで設定しても構わないが、あとで固定IPアドレスを設定する)
1. Update Software
   * `Skip`をクリック
1. Setup Complete
   * `Done`をクリック
1. 再起動する
   * メニューバーから`Shutdown`を選択
   * `Reboot`をクリック
