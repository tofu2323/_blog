+++
date = "2017-01-11T23:24:22+09:00"
slug = "rails-trial2"
tags = ["Ruby on Rails","learning"]
categories = ["Web"]
title = "Ruby on Rails チュートリアルをやってみている2"

+++

### 第2章 Toyアプリケーション

#### 2.1 アプリケーションの計画  
どうせなので、Herokuデプロイ前に`rails server`してみようと思ったが、
http://localhost:3000 につながらない。  
http://0.0.0.0:3000/ だと繋がった。。。  
Macでlocalhostが何か違う？？　　



```
$ git commit -am "Add hello"
$ heroku create
$ git push heroku master
```
これ、今回はサクッといった。  
herokuすごい！  

からの
```
$ heroku open
```

`$ rails generate scaffold User name:string email:string`  
すごい！けど、謎が深まるばかり。。


##### 2.2.1 ユーザーページを探検する
探検できなかった。  
http://0.0.0.0:3000/users  
```
ArgumentError in UsersController#index
key must be 32 bytes
```

[ここ](https://github.com/rails/rails/issues/26694)によると

> It has been fixed by #25758 and will be available to use when Rails 5.0.1 is released, thanks for the report!   

とのこと。。

ということで、
```rb
gem 'rails',        '5.0.1'
```
にして、`$ bundle update`したらいけた。
けど、チュートリアルどうなのこれ？  



`heroku logs --tail`
