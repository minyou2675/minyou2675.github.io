---
title:  "[Github 깃허브 블로그 만들기] 2편 지킬(jekyll) 적용하기"
excerpt: "깃허브에 지킬(jekyll)테마를 적용해봅시다."

categories:
  - Github
tags:
  - [Blog, Github, Git]

toc: true
toc_sticky: true
 
date: 2023-04-11
last_modified_at: 2023-04-11
---

## 루비랑 jekyll 설치는 로컬 확인용이므로 필수는 아니므로 바로 테마 고르기 넘어가셔도 좋습니다.

## **루비 설치**

jekyll은 언어로 ruby를 사용합니다.

https://rubyinstaller.org/downloads/

위 링크에서 ruby installer devkit x86bit를 다운받습니다. 설치할 때는 따로 체크할 거 없이 계속 next만 누르면 됩니다.

> x86bit를 다운받는 이유는 jekyll이 32비트를 지원합니다.

## **jekyll 설치**

ruby를 받았으면 Start Comman prompt with Ruby를 실행합니다. 터미널에 아래 명령어로 루비가 설치되어 있는지 확인하고 

```
ruby -v
```

![image](https://user-images.githubusercontent.com/62383521/231188433-e828d9ca-4776-46cf-af24-ef38598c2fe8.png)
"이런게 뜨면 정상적으로 설치 되었다는 소리"

이제 jekyll을 설치해줍니다.

```
gem install jekyll
```

jekyll도 정상 설치 되었는지 확인합니다.

> 사실 이쯤에서 jekyll이 깔리지 않아서... 로컬에서 서버를 띄우는 방식으로 확인은 못하고 바로 깃허브로 올리게 되었습니다.

## **테마 고르기** 

이제 우리가 사용할 블로그에 적용할 jekyll 테마를 골라줍니다. 아래 사이트가 테마가 많아서 좋은데, 어디서 찾든 딱히 상관은 없습니다.

**[http://jekyllthemes.org/](http://jekyllthemes.org/)**


저는 흰검을 좋아해서 아래 monos라는 테마를 선택했습니다.



http://jekyllthemes.org/themes/monos/

테마별로 hompage가 있는데 깃허브 레포지토리랑 연결됩니다. 들어가서 깃 클론을 해줍니다. 모노의 경우에는 이렇습니다.

```
git clone https://github.com/ejjoo/jekyll-theme-monos.git
```

이제 jekyll-theme-monos라는 폴더가 로컬에 생성되었을 겁니다.

### ****테마 적용하기****

만약 기존에 username.github.io 폴더에서 하던 작업물들이 있으면 그대로 복사한 뒤 jekyll-theme-monos 폴더에 복붙 합니다.

다시 복붙 한 파일들을 username.github.io로 넣고 git add ... git commit 후 git push를 해줍니다.

잠시 기다린 후, 깃허브 블로그에 들어가면

![image](https://user-images.githubusercontent.com/62383521/231188537-6c407df0-5a9e-48e7-be89-b25464d6a8be.png)

jekyll 테마가 적용된 블로그를 확인할 수 있습니다. 

이제 포스트를 올리려면 \_posts에 마크다운 파일을 올리고 파일 이름이나 형식도 정해져 있는데 그거는 다음 장에 다뤄보겠습니다.
