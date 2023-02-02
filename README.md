# docker-spring-sample
Dockerを使用してSpring Bootアプリケーションを実行、デバッグするためのサンプルプログラムです。

## インストールするもの
- [Docker](https://www.docker.com/)
- [Git for Windows](https://gitforwindows.org/)
- [Intellij IDEA](https://www.jetbrains.com/ja-jp/idea/)

## 実行手順
1. **Git for Windows**を起動してプロジェクトをローカルにCloneする
1. **Intellij IDEA**を起動して、1を開く
1. **Intellij IDEA**のメニューで、`Run > Edit Configurations...`を選択する
1. **Run/Debug Configurations**ダイアログで＋ボタンを押下し、`Remote JVM Debug`を選択し、以下を設定する  
    - Name: Remote Debug
    - Debugger mode: Attach to remote JVM
    - Transport: Socket
    - Transport: Socket
    - Host: localhost
    - Port: 5005
1. **docker-compose.yml**を開き、`services`の行で緑矢印をクリックする  
    → **Build Log**ウィンドウに`Starting docker_spring_sample_web_1 ... done`が表示されることを確認する   
1. メニュー右上の`Run Configuration`プルダウンで`Remote Debug`を選択し、Debugボタン（緑色の虫マーク）を押下する
1. 下記のファイルを開いて、11行目の枠外をクリックしてブレークポイントを設定する  
    `src > main > java > com.sample.dockerspring > controller > SampleController`
1. ブラウザで http://localhost:18080/ にアクセスし、ブレークポイントで止まることを確認する
