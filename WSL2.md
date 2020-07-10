## WSL2(Arch)でmatplotlibのグラフを表示する
### 注意点
- パッケージ qt5-base をインストール。`sudo pacman -S qt5-base`

- python にパッケージ PyQt5 をインストール。`pip install PyQt5`

- バックエンドの設定をmatplotlibrcに記述。参考: https://note.nkmk.me/python-matplotlib-matplotlibrc-stylesheet/

- 出力先のディスプレイ設定。 https://www.google.com/search?q=WSL2+DISPLAY

- VcXsrvの設定。 https://www.google.com/search?q=WSL2+VcXsrv
  1. Multiple windows
  1. Start no client
  1. **`Native opengl` のチェックを外す。** これがオンになっていると`glxgears`などのデモがガクガクになる。
  
  1. `Disable access control` をチェック。これをしないと "Authorization required, but no authorization protocol specified" のエラー。
  
  1. **ファイアウォールの許可「パブリック」にもチェック。** これを忘れても**全くエラーが出ない**ので危険 :exclamation:
