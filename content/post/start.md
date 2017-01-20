+++
date = "2017-01-09T12:22:58+09:00"
tags = ["Hugo"]
categories = ["Web"]
slug = "start"
title = "スタートメモ"

+++


## [Hugo](http://themes.gohugo.io/)  

https://staticsitegenerators.net/

`$ brew install hugo`
```.sh
==> Downloading https://homebrew.bintray.com/bottles/hugo-0.18.1.sierra.bottle.t
######################################################################## 100.0%
==> Pouring hugo-0.18.1.sierra.bottle.tar.gz
==> Caveats
Bash completion has been installed to:
  /usr/local/etc/bash_completion.d
==> Summary
🍺  /usr/local/Cellar/hugo/0.18.1: 32 files, 16.3M
```

`$ hugo version`
```.sh
Hugo Static Site Generator v0.18.1 BuildDate: 2016-12-30T02:12:41+09:00
```

`$ hugo new site blig`
```.sh
Congratulations! Your new Hugo site is created in /Users/fumiya/Dev/hugo/blog.

Just a few more steps and you're ready to go:

1. Download a theme into the same-named folder.
   Choose a theme from https://themes.gohugo.io/, or
   create your own with the "hugo new theme <THEMENAME>" command.
2. Perhaps you want to add some content. You can add single files
   with "hugo new <SECTIONNAME>/<FILENAME>.<FORMAT>".
3. Start the built-in live server via "hugo server".

Visit https://gohugo.io/ for quickstart guide and full documentation.
```

```.sh
cd themes
git clone https://github.com/kakawait/hugo-tranquilpeak-theme.git
```

```.sh
$ hugo new post/start.md --editor="atom"
```

```default.md
---
title: ""
slug: ""
categories:
  - ""
tags:
  - ""
---

```

`$ hugo server -v`
