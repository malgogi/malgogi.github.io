---
layout: post
title:  jekyll로 블로그 생성해보기
description: jekyll 프로젝트 셋팅 방법
comments: true
date:   2020-01-27
categories: [jekyll]
tags: [ jekyll ]
---

# Jekyll 사용법

## 사용 준비

### 1. rvm 설치

ruby version manager입니다. 일부 버전 호환성 때문에 rvm을 설치하여 ruby의 버전을 관리해줍니다.

```bash
# rvm isntall
curl -sSL https://raw.githubusercontent.com/rvm/rvm/master/binscripts/rvm-installer | bash -s stable
```

### 2. ruby 버전 변경

```bash

# version check
rvm list

# rvm lastest version install
rvm install ruby --latest

# change ruby version in current terminal
rvm use ${RUBY_VERSION}
```

### 3. jekyll install

```bash
sudo gem install bundler jekyll
```

### 4. create project

```bash
jekyll new ${PROJECT_DIR}
```

### 5. test it

local server를 start 합니다.
해당 명령을 수행하고 localhost:4000에서 확인하시면 됩니다.

```bash
cd ${PROJECT_DIR}
jekyll serve
```

### 6. create github repository

github repository이름을 다음과 같이 생성해줍니다.

```bash
${USER_NAME}.github.io
```

### 7. remote repository binding

다음과 같이 jekyll로 생성된 프로젝트에 remote repository를 추가해줍니다. 
Repository 생성시에 친절한 가이드가 설명이 되어 있어서 해당 방식을 따르는 것이 좋습니다.

```bash
cd ${PROJECT_DIR}

git init
git remote add origin https://github.com/malgogi/malgogi.github.io.git
```

### 8. publish

다음과 같이 프로젝트를 올립니다.
그 후 다음과 같은 사이트에 접속해봅니다.

https://${USER_NAME}.github.io/

```bash
cd ${PROJECT_DIR}

git add .
git commit -m "init"
git push origin master
```

## 출처

- [jekyll 사이트](https://jekyllrb-ko.github.io/)
- [rvm 공식 사이트](https://rvm.io/rvm/install)