# Math-Textbooks-UG

Math-Textbooks-UG は，学部～大学院初年度レベルの数学教科書シリーズの執筆を行うプロジェクトであり，自己完結性・網羅性・厳密性・一貫性を備えた教科書の実現を目指しています．

本リポジトリのコラボレーターを随時募集しています．

## シリーズ

（記載予定）

## ビルド方法

同梱の TeXソースファイルから，ローカルで文書をビルドすることもできます．

### 環境

TeX Live 2024 が必須です．fullスキームがインストールされていることが望ましいです．

LuaLaTeX でのビルドを推奨していますが，XeLaTeX でもビルド可能です（(u)pLaTeX には対応していません）．割と最近追加されたパッケージやオプションも使用しているため，ビルド前には必ず TeX Live をアップデートしてください．

### 手順

1. 以下をコマンドラインで実行．
    ```powershell
    cd src/???-UG
    ```
    ただし，`???-UG` はビルドしたい文書に紐づいた名前（上記「シリーズ」を参照）．  
    例えば，『学部数学のための論理学』をビルドしたい場合は，
    ```powershell
    cd src/01-Logic-UG`
    ```

2. 以下をコマンドラインで実行．
    - LuaLaTeX の場合
    ```powershell
    latexmk -norc -r .latexmkrc -lualatex main
    ```
   - XeLaTeX の場合
    ```powershell
    latexmk -norc -r .latexmkrc -xelatex main
    ```
    ただし，ホームディレクトリに (.)latexmkrc を設置していない場合は
    ```powershell
    latexmk -lualatex main
    ```
    ```powershell
    latexmk -xelatex main
    ```
    のみでも可．
