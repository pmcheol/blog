---
layout: post
title: "Select Upsert"
categories: sql
---

## SELECT 결과를 INSERT 하자 

```sql
INSERT INTO A
(id, name)
SELECT id, 'NONAME'
FROM B 
WHERE B.date = '1986-11-11';
```

<br/>

## SELECT 결과를 UPDATE 하자

```sql
UPDATE A, B
SET A.name = B.name
WHERE A.id = B.id;
```
