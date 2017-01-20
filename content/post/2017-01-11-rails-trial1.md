+++
date = "2017-01-11T22:40:04+09:00"
slug = "rails-trial1"
tags = ["Ruby on Rails","learning"]
categories = ["Web"]
title = "Ruby on Rails チュートリアルをやってみている"

+++

## Ruby on Rails チュートリアル

アプリ開発にRailsを使ってみようということで[Ruby on Rails チュートリアル](https://railstutorial.jp/)を一通りやってみる。  

Rubyに触ったことはない。  
RailsがなんかWebアプリ開発によく使われているという程度の知識。

プログラミング歴2年。Javaから入って今一番触っている言語はTypeScriptという私です。  
Macを使っている。

感想・ハマったことなどメモ。

### 第1章

#### 1.2.1 開発環境
Cloud9 を推奨されているけどMacにすでに入っているIntelliJ IDEAを使用。。。  
あとでherokuにpushするときに若干ハマる。  
IDEAのプロジェクトのファイル構成がよくわかっていない。  

#### 1.3 最初のアプリケーション
構成とかアーキはRailsで標準的なものがある感じ？？  
どういう風にrailsに乗って行くべきか。。  

会社の開発（Spring Boot + Vue.js)ではroutingもクライアントでやっていてそれが普通だと思っていたけど
そもそもサーバーでやるのが一般的なの？？


.GemFileというもの
```
source 'https://rubygems.org'

gem 'rails',        '5.0.0.1'
gem 'puma',         '3.4.0'
gem 'sass-rails',   '5.0.6'
gem 'uglifier',     '3.0.0'
gem 'coffee-rails', '4.2.1'
gem 'jquery-rails', '4.1.1'
gem 'turbolinks',   '5.0.1'
gem 'jbuilder',     '2.4.1'

group :development, :test do
  gem 'sqlite3', '1.3.11'
  gem 'byebug',  '9.0.0', platform: :mri
end

group :development do
  gem 'web-console',           '3.1.1'
  gem 'listen',                '3.0.8'
  gem 'spring',                '1.7.2'
  gem 'spring-watcher-listen', '2.0.0'
end

# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]
```
package.json的なもの。。。  
coffee-railsとか、sass-railsとか、、クライアントサイドもrailsでかけるのね。。  
なんかそもそもrailsとかWebアプリについて勘違いしていた気がする。  

開発するWebアプリでは、いつも通りクライアントとサーバは疎な感じにして
RailsはAPIを提供するのみにする？？  

**そうした場合とそうでない場合のメリット・デメリットを知る必要がある**

#### 1.5 デプロイする  
また、Herokuでハマった。  
とりあえずは、pushする時のルートが違っていたからだけどいまいちheokuを理解しきれていない。  

```
$ cd ~/workspace
$ rails _5.0.0.1_ new hello_app
```
とした時、pushするのは
`~/workspace`ではなく`~/workspace/hello_app`
