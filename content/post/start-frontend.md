+++
tags = ["Vue.js"]
categories = ["Web"]
slug = "start-frontend"
title = "フロントエンド検討メモ"
date = "2017-01-09T13:45:38+09:00"

+++

## vue.js

使い慣れているのは1.x系だけど確実に2.x系を使うべき。  
1.x系はなかったことにされている雰囲気。  


2.x系少しキャッチアップにコストがかかる。  
どうせなら合わせて色々使ってみる？  


### 検討事項

#### vue-cli  
これを使えばwebpackやgruntがいらない？？

### vuex
使うのが普通？  
Fluxというもの  
[参考](https://medium.com/@sotayamashita/%E6%BC%AB%E7%94%BB%E3%81%A7%E8%AA%AC%E6%98%8E%E3%81%99%E3%82%8B-flux-1a219e50232b#.7ofaks2rk)  

* データフローが一方向なのがすごいらしい  
  ACTION -> DISPATHCER -> STORE -> VIEW -> ACTION  
  Vuexは以下？  
  Action -> Mutations -> State -> Vue Component -> Action



## よく見かけるもの  

### Nginx

<!--more-->
