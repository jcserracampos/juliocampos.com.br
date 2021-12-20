---
title: Instalando Ruby antigo no M1
date: "2021-07-15T16:51:00.000Z"
layout: post
draft: true
category: "Blog"
tags:
  - "arm64"
  - "Ruby"
description: "Uma nova arquitetura, novos desafios"
---

RUBY_CFLAGS="-Wno-error=implicit-function-declaration" rbenv install 2.6.3

gem install sassc -- --disable-march-tune-native
bundle config --local build.sassc --disable-march-tune-native


brew install --build-from-source v8@3.15
  bundle config build.libv8 --with-system-v8
  bundle config build.therubyracer --with-v8-dir=$(brew --prefix v8)

Export openssl
   export LIBRARY_PATH=$LIBRARY_PATH:/opt/homebrew/Cellar/openssl@1.0/lib
   https://github.com/brianmario/mysql2/issues/795


     831  npm install chromedriver --chromedriver_filepath=/bin/chromedriver
  832  yarn chromedriver --chromedriver_filepath=/bin/chromedriver
    823  cp ~/Downloads/chromedriver /usr/local/bin