# Languages

Date: 2015-10-01 11:08
Tags: []
Categories: []

---

## Prelude

- Bash     : Refs: [linux-shell-script](linux-shell-script)
- Java     : Refs: [java](java)
- Markdown : Refs: [markdown](markdown)
- Ruby     : Refs: [ruby](ruby)
- UML      : Refs: [uml](uml)

## Languages

### Perl

- LTSV parser

        cat accesslog | perl -F'\t' -nale '%h=map{split/:/,$_,2}@F;print"$h{time}\t$h{ua}"'

    Refs: [LTSVログをパースする最強のワンライナー集&middot;DQNEO起業日記](http://dqn.sakusakutto.jp/2014/02/ltsv_parser_oneliner.html)

- 最短一致にする場合には数量子の後ろに ? を付けます。

        s/a+?/1/;

- 置換
    - 複数行置換

            perl -0pe 's/aaa\nbbb/ccc/m' foo.txt

        - 複数の空行を1つに置換

                perl -0pe 's/\n\n\n/\n/m' foo.txt

    - 置換後保存

            perl -pi -e 's/aaa/ccc/g' foo.txt

    - マッチ全体を格納(後方参照)

            perl -0pe 's/hoge/$&+fuga/m' foo.txt

- ドキュメントを読む

        perldoc hoge
        perldoc perldoc
        perldoc perlintro

### Python

- pip update

        sudo pip install pycrypto

### Node.js

- npm install

        sudo npm install -g eslint

- npm uninstall

        sudo npm uninstall -g eslint

- npm自身をupdate

        sudo npm update -g npm

- すべてのGlobalパッケージをアップデート

        sudo npm update -g

#### Notes

- msys2の場合global installしたパス(node_modules)が含まれなそうなのでNODE_PATH設定したほうがよさそう

        export NODE_PATH=/mingw64/lib/node_modules

