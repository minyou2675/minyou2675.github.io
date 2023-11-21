<!-- ---
title:  "Django User 사용"
excerpt: "Abstract User, Abstract Base User"

categories:
  - Django
tags:
  - [Blog, Django]

toc: true
toc_sticky: true
 
date: 2023-11-05
last_modified_at: 2023-11-05
---

## User 모델
기본적으로 사용하는 user 모델은 auth라는 모듈에 있는 user 클래스를 가져다가 사용하게 된다.

### 유저 모델

### 비밀번호 암호화
create_user 메소드를 사용하면 user class의 메소드를 통해 비밀번호를 암호화 시킬 수 있다.
암호화는 SHA-256알고리즘을 적용한 단방향 해시 알고리즘이다. -->