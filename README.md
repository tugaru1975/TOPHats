# 自作ハットの追加方法
### 1.このリポジトリを[Fork](https://github.com/tugaru1975/TOPHats/fork)する
### 2.Forkしたリポジトリの`hats`に自作した帽子スキンをアップロード
### 3.アップロードしたら`CustomHats.json`にコードを追加する
```
        {
            "name": "題名",
            "author": "制作者名",
            "condition": "None",
            "resource": "帽子の画像名.png",
            "backflipresource": "帽子の_back_flip用の画像名.png",
            "backresource": "帽子の_back用の画像名.png",
            "flipresource": "帽子の_flip用の画像名.png",
            "climbresource": "帽子の_climb用の画像名.png",
            "bounce": true,
            "adaptive": true
        },
```  
**※いらないコードは消してください**  
**※`,`を最後の行では削除してください**
#### コードの説明
`"name"` : 帽子の題名  
`"author"` : 制作者名  
`"condition"` : よくわからない。`"None"`で機能する。  
`"resource"` : 帽子画像を決められる。  
`"backflipresource"` : クルーの反対向きでの背面の帽子画像を決められる。  
`"backresource"` : クルーの背面の帽子画像を決められる。  
`"flipresource"` : クルーの反対向きでの帽子画像を決められる。  
`"climbresource"` : クルーの梯子の帽子画像を決められる。  
`"bounce": true` : 帽子を跳ねさせることが出来ます。  
`"adaptive": true` : クルーの色に帽子画像を変えることが出来ます。
### 4.TOPに対応させる
AmongUsファイルのデフォルト状態なら  
Steam : `C:\Program Files (x86)\Steam\steamapps\common\Among Us`  
Epic : `C:\Program Files (x86)\Epic Games\AmongUs`にある、  
`BepInEx` > `config` > `com.tugaru.TownOfPlus.cfg`を開きます。  
**開けない場合は`.cfg`を`.txt`にします。**  
次に下にスクロールしていくと
```
[HatURL]

# Setting type: String
# Default value: https://raw.githubusercontent.com/tugaru1975/TOPHats/master,https://raw.githubusercontent.com/ユーザー名/プロジェクト名/master
HatURL = https://raw.githubusercontent.com/tugaru1975/TOPHats/master,https://raw.githubusercontent.com/ユーザー名/プロジェクト名/master
```  
という部分があるので`/ユーザー名/`と`/プロジェクト名/`の部分をそれぞれ自身のgithubユーザー名とプロジェクト名(デフォルトは`TOPHats`)にしてください。  
**`.txt`にしている場合は`.cfg`に戻してください。**  
そしてAmongUsを開いて導入されていたら完了です。
### 5(任意).TOPでの実装
自身のプロジェクトをこのプロジェクトにプルーリクエストしていただければTOPの方で実装いたします。  
**オリジナルの帽子を削除している場合は元に戻してからプルリクしていただけると嬉しいです。**
# 自作ハットの試し方
AmongUsファイルのデフォルト状態なら  
Steam : `C:\Program Files (x86)\Steam\steamapps\common\Among Us`  
Epic : `C:\Program Files (x86)\Epic Games\AmongUs`にある、  
`TownOfPlus`>`SkinTest`のなかに自作した帽子画像を入れると試すことが可能です。  
この時`帽子名_adptive.png`のようにすると[コマンド](#コードの説明)を対応させることが出来ます。
