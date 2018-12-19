---
layout: post
title: "github multiple ssh key 사용"
categories: develop
---

## 1. ssh key 준비  

> ssh key를 2개를 생성하고, 적절한 네이밍과 ~/.ssh 폴더에 잘 정리하여 저장합니다.

```jshelllanguage
$ ssh-keygen -t rsa -C "user1@address.com"
$ ssh-keygen -t rsa -C "user2@address.com"
```
```jshelllanguage
$ cd ~/.ssh
$ ls

id_rsa_user1
id_rsa_user1.pub
id_rsa_user2
id_rsa_user2.pub
```
<br/>

## 1-1. ssh key 등록 

> github에서 해당하는 repository에 `deploy keys`에 공개키를 등록합니다.

<br/>

## 2. ssh config 작성

> custom한 host이름으로 적절한 ssh key를 매핑하기 위해 config 파일을 작성합니다.   

```jshelllanguage
$ vi ~/.ssh/config
```
```jshelllanguage
#user1
Host github.com-user1
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa_user1

#user2
Host github.com-user2
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa_user2
```
<br/>

## 3. host 주소 변경 

> remote 주소를 custom하게 작성한 host 이름으로 변경 합니다.

```jshelllanguage
$ cd YOUR_WORKING_SPACE_FOLDER
$ git remote remove origin
$ git remote add origin git@github.com-user1:USER_NAME/REPOSITORY.git
``` 
<br/>

## 4. git push 

```jshelllanguage
$ git push
```
<br/>

## 4-1. git commit

> commit 할 때 author를 지정할 수 있습니다.

```jshelllanguage
$ git commit --author="authorName <email@address.com>"
```
<br/>
