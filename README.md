## 各バージョン

Rails 5.1.6
ruby 2.3.1
npm 5.6.0
node 9.8.0

## ディレクトリ構造

appl ディレクトリ以下には rails 用のファイル、client ディレクトリ以下には React 用のファイルが入っている。

## gitignore について

通信負荷がかかる node_module(Javascriot のライブラリ)は git 管理下から既に外している。その他個々人でこれは管理下に置くのはセキュリティの面からも git push・git pull のパフォーマンス面からも不適切だと考えるのであれば、各自 gitignore を更新するのが望ましい。

ただし既に git の管理下にあるものを管理外にするときは gitignore に記入するだけでは不十分。詳しくは google で。

## appl ディレクトリの立ち上げ方

@local cd appl/
@local rails s

## client ディレクトリの立ち上げ方

前提:
node と npm がインストールされていること。バージョンは下記の通り。
node v9.8.0
npm v5.6.0
各々のローカルマシンの node と npm のバージョンが違えば危険なので出来ればこのバージョンに統一してほしい。

@local cd client/
@local npm install
@local npm start
