---
layout: post  
title: "mysql Explain"  
subtitle: "Mysql 실행계획 알아보자"  
categories: mysql
---

## Mysql Explain 

| type            | 설명                                                                        |
|-----------------|---------------------------------------------------------------------------|
| system          | 테이블에 단 한개의 데이터만 있는 경우                                                     |
| const           | SELECT에서 Primary Key 혹은 Unique Key를 살수로 조회하는 경우로 많아야 한 건의 데이터만 있음         |
| eq_ref          | 조인을 할 때 Primary Key                                                       |
| ref             | 조인을 할 때 Primary Key 혹은 Unique Key가 아닌 Key로 매칭하는 경우                        |
| ref_or_null     | ref 와 같지만 null 이 추가되어 검색되는 경우                                             |
| index_merge     | 두 개의 인덱스가 병합되어 검색이 이루어지는 경우                                               |
| unique_subquery | 다음과 같이 IN 절 안의 서브쿼리에서 Primary Key가 오는 특수한 경우                              |
| index_subquery  | unique_subquery와 비슷하나 Primary Key가 아닌 인덱스인 경우                             |
| range           | 특정 범위 내에서 인덱스를 사용하여 원하는 데이터를 추출하는 경우로, 데이터가 방대하지 않다면 단순 SELECT 에서는 나쁘지 않음 |
| index           | 인덱스를 처음부터 끝까지 찾아서 검색하는 경우로, 일반적으로 인덱스 풀스캔이라고 함                            |
| all             | 테이블을 처음부터 끝까지 검색하는 경우로, 일반적으로 테이블 풀스캔이라고 함                                |
