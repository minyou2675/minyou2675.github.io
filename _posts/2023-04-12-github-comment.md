---
title:  "[깃허브 페이지] 깃허브 페이지에 댓글 기능추가"
excerpt: "깃허브에 페이지에 코멘트를 넣어봅시다."

categories:
  - Github
tags:
  - [Blog, Github, Git]

toc: true
toc_sticky: true
 
date: 2023-04-12
last_modified_at: 2023-04-12
---
### **utterances 앱 설치하기**

> 블로그라면 댓글이 있어야 하지 않을까?

**Jekyll** 기반의 페이지들은 Disqus를 쓴다고 하는데, 나는 그런 거 없이 아예 처음부터 utterances를 적용해보겠다.

먼저 링크에 들어가 설치한다.

[https://utteranc.es](https://utteranc.es/)

![image](https://user-images.githubusercontent.com/62383521/231484513-4c588862-ef67-47da-9ddb-d8a78a908591.png)

코멘트를 이슈로 저장할 레포르 선택한다. 나는 그냥 깃허브 페이지 레포로 설정했다.

![image](https://user-images.githubusercontent.com/62383521/231484548-ee20b80e-44af-4968-880b-382ddab3aae4.png)

그리고 코멘트 기능을 연결한 레포로 정한다. username/repository.name 형식으로, 깃허브 페이지 레포를 지정한다. 코멘트로 이슈를 생성할 때는 페이지의 파일명을 매핑하기로 한다. ( 포스트 제목으로 매핑하기에는 변동 가능성이 있으므로)

그러고 마지막 줄에 가면 이렇게 script가 나온다. 그대로 복사한다.

![image](https://user-images.githubusercontent.com/62383521/231484589-1d992732-07dd-4e9d-9be9-a4e40c2684fd.png)

깃허브 페이지 레포지토리 폴더에서 \_layouts/post.html 에서 아래와 같이 스크립트 삽입해준다.

![image](https://user-images.githubusercontent.com/62383521/231484607-af4974cb-76eb-46a1-a49a-956d3de059f8.png)

## **마무리**

![image](https://user-images.githubusercontent.com/62383521/231484629-7f0b273a-8bee-4df8-a19d-f355bdceb18e.png)

그러면 이와 같이 댓글을 삽입할 수 있다.