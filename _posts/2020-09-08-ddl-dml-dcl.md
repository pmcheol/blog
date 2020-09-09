---
layout: post
title: "DDL, DML, DCL 정리"
categories: develop
---

## 1. DDL(Data Definition Language): 데이터를 정의하는 언어

- CREATE: 생성
- DROP: 삭제
- ALTER: 수정
- TRUNCATE: 테이블 데이터 제거

<br/>

## 2. DML(Data Manipulation Language): 데이터 검색, 등록, 삭제, 갱신을 위한 언어

- SELECT: 검색
- INSERT: 삽입
- UPDATE: 수정
- DELETE: 삭제

<br/>

## 3. DCL(Data Control Language): 엑세스 제어 언어

- GRANT: 권한부여
- REVOKE: 권한제거

### 3-1. 권한목록

- CONNECT: 접속권한
- SELECT: 검색권한
- INSERT: 등록권한
- UPDATE: 수정권한
- DELETE: 삭제권한
- USAGE: 스키마, 함수, DB 개체를 사용할 수 있는 권한
