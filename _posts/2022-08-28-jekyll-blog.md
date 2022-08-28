---
layout: post  
title: "BLOG 만들기 with Jekyll"  
subtitle: "jekyll 활용하여 블로그를 만들어 본다. (2022-08 기준)"  
categories: Jekyll
---

## Jekyll 

Ruby 기반으로 만든 설치형 블로그

## Getting Started

```bash
$ gem install bundler jekyll
```

<br/>

만약 M1 에서 에러가 발생한다면  
Ruby 버전을 의심해야 한다.  
버전 관리를 위해 `rbenv` 사용한다.

```bash
$ brew install rbenv
```

```bash
$ rbenv install -l
```
```bash
...
2.6.10
...
```

<br/>

적절한 버전을 찾았다면 아래와 같이 파라미터를 넣어서 (1줄임)  
적절한 버전을 설치하고 적용한다.

```bash
$ CFLAGS='-Wno-error=implicit-function-declaration'  
RUBY_CONFIGURE_OPTS='--with-readline-dir=/usr/local/opt/readline/'  
arch -x86_64 rbenv install 2.6.10
```
```bash
$ rbenv global 2.6.10
```

<br/>

잊지 않고 환경 변수도 설정한다. 
```bash
$ vi ~/.bash_profile
```
```shell
...
export PATH={$Home}/.rbenv/bin:$PATH && \
eval "$(rbenv init -)"
```
```shell
$ source ~/.bash_profile
```

<br/>

다시 설치를 완료하고 처음 블로그를 만들어 본다.  

```bash
$ gem install bundler jekyll
$ mkdir my-blog
$ cd my-blog
$ jekyll new ./ # 블로그 생성 
$ bundle exec jekyll serve # 블로그 서버 실행 (http://localhost:4000)
```

<br/>
