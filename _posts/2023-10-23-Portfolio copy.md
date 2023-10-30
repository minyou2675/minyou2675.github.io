---
title:  "Portfolio_COPY"
excerpt: "안녕하세요! 소개 페이지입니다."
layout: about
toc: true
toc_sticky: true

 
date: 
last_modified_at: 
---
 <link rel="stylesheet" href="/public/css/portfolio.css">
<script src="https://kit.fontawesome.com/939690c74b.js" crossorigin="anonymous"></script>

<style>
    .grid-container{
        display:grid;
        grid-template-columns:1fr 1fr;
        /* border-style:solid; */
        align-content: space-evenly;
        margin-bottom:100px;
    }
    .left-container{
    padding-right:5rem;
    }
    .social-col{
      display:flex;
      flex-direction:row;

    }
</style>
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-DQE38KV51N"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-DQE38KV51N');
</script>


<div class="grid-container">
<div style="margin-left:10px;">
 <div class="wrapper">
    <div class="img-area">
      <div class="inner-area">
        <img src="/images/이력서사진.jpg" alt="">
      </div>
    </div>
    <div class="icon arrow"><i class="fas fa-arrow-left"></i></div>
    <div class="icon dots"><i class="fas fa-ellipsis-v"></i></div>
    <div class="name">김유민</div>
    <div class="about">SW Engineer</div>
    <div class="social-icons">
      <a href="https://github.com/minyou2675" class="fb"><i class="fa-brands fa-github"></i></a>
      <a href="#" class="https://www.linkedin.com/in/yumin-kim-a58345262/"><i class="fa-brands fa-linkedin" style="color: #3371db;"></i></a>
      <a href="#" class="insta"><i class="fab fa-instagram"></i></a>
    </div>
    </div>
  </div>
 <div>
<h3> 클라우드 시대에 인프라 역량을 겸비한 SW엔지니어 김유민입니다</h3>
<br>저는 처음에는 생명공학을 전공했지만 IT에 대한 관심을 바탕으로 컴퓨터과학을 전공하기 시작했습니다. 이후에는 다양한 IT동아리, 공모전 등에 활동하면서 역량을 키웠으며 자격증과 전공을 공부하면서 전문성을 강화하였습니다. 앞으로도 지속적인 관심을 가지고 발전하는 IT전문가로 성장하겠습니다.
</div> 
</div>


## Education
---

### 상명대학교

<div class="grid-container">
    <div>
    <h4>컴퓨터 과학 전공</h4>
    <h5>전체평점 (3.46/4.5)</h5>
    <h5>전공평점 (3.96/4.5)</h5>
    <h4>생명공학 복수 전공</h4>
    </div>
    <br>
    2017.03 ~ 2024.03
    <br>졸업예정


</div>



<!--## SKILLS 
JavaSciprt Python Django React TypeScript-->

## Experiences
---
<!-- 
## AWS 빅데이터 경진대회(AWS 주관 산학 경진대회)
### 지방 인프라 데이터 플랫폼
개발기간 23.06 ~ 23.09

제가 맡은 역할

* 팀장으로서 문서관리
* React 이용하여 GUI 전체 개발
* Ajax를 활용하여 비동기 API 호출
* NextJs기반 API 개발(S3와 연동하여 데이터 분석) -->

## 개인 프로젝트
---

<div class="grid-container">
<div class="left-container">
<h3>커플 다이어리 웹 페이지 개발</h3>
<a href="https://github.com/minyou2675/couple_diary_project">깃허브링크</a> 
<img src="/images/github.png" alt="" width="30px" height="30px">
<br>개발기간 23.06 ~ 진행 중
<br>'클라우드 프로그래밍' 수업 시간에서 클라우드 서비스를 이용해 배포하는 기말 프로젝트를 수행하며 동시에 여자친구와 맞춤형 커플 다이어리를 만들기 위한 목적으로 커플 다이어리 웹 어플리케이션을 개발했습니다. 기말고사때 PaaS-TA라는 개방형 클라우드 플랫폼에 배포하여 최종 평가를 받았으며 A+이라는 성적을 얻을 수 있었습니다.
</div>
<div>
<h4>사용 기술 스택</h4>
<li>Python</li>
<li>Django</li>
<li>JavaScript</li>
<li>Docker</li>

<h3>제가 맡은 역할</h3>
<li>Entity 작성 및 달력 기반 CRUD 기능 구현</li>
<li>DRF기반 게시판 작성 등 Restful CRUD API 개발 진행</li>
<li>Swagger로 API 자동 문서화 진행</li>
<li>Serializer로 데이터 직렬화 수행 진행</li>
<li>Locust를 이용한 부하테스트</li>
<li>Docker 컨테이너 기반 개발 환경 구축</li>
</div>
</div>

## 클라우드 클럽(동아리)
--- 

<div class="grid-container">
<div class="left-container" style="margin-top:0rem;">

<h3>Terraform을 이용한 인프라 구축</h3>
<a href="https://github.com/minyou2675/Yanadoo_Terraform">깃허브링크</a> 
<img src="/images/github.png" alt="" width="30px" height="30px">
<br>
개발기간 23.05 ~ 23.06
<br>
Terraform을 이용하여 IaC를 이해하고, AWS 고객사례를 참고하여 야나두의 클라우드 아키텍쳐를 분석하고 이를 Terraform으로 구축하는 실습과 코드리뷰 스터디를 진행했습니다. 
</div>
<div>
<h4>사용 기술 스택 </h4>
<li>HCL</li>
<li>Terraform</li>
<li>AWS(RDS, NAT, Gateway, Waf, Load balancer)</li>

<h4>이런 걸 배웠어요</h4>
<li>HCL 문법</li>
<li>IaC 개념을 통해 인프라를 코드로 구현하는 것의 유용성</li>
<li>클라우드 아키텍쳐와 인프라에 대한 이해</li>
<li>Terraform Backend를 이용한 tf.state 관리 및 인프라 일관성 유지</li>
</div>
</div>

<!-- <div class="grid-container">
<div class="left-container" style="margin-top:0rem;">

 <h3>Dokcer K8S 기반 투두메이트 웹 페이지 배포 </h3>

<a href="https://github.com/cloud-club/ToDoMate">깃허브링크 
<img src="/images/github.png" alt="" width="30px" height="30px"></a>
<br>
개발기간 23.03 ~ 23.04
<br>REST API를 구축하여 Todomate 페이지를 구축하고 k8s 환경을 설정하여 실제 배포 환경을 구축하는 실습을 진행 했습니다.
</div>
<div>
<h4>사용 기술 스택</h4>
<li>Docker</li>
<li>K8S</li>
<li>Django</li>

<h4>이런 걸 배웠어요</h4>
<li>Docker를 이용한 어플리케이션 컨네이너화</li>
<li>k8s를 통한 어플리케이션 배포</li>
</div>
</div> -->

<div class="grid-container">
<div class="left-container" style="margin-top: 0rem;">

<h3>쉘 스크립트 프로젝트</h3>
<a href="https://github.com/minyou2675/CloudClub">깃허브링크 
<img src="/images/github.png" alt="" width="30px" height="30px"></a>
<br>
개발기간 22.10 ~ 22.11
<br>
리눅스 환경에서 쉘 스크립트를 이용한 업무 자동화에 대한 관심사를 기반으로 쉘 스크립트 스터디를 진행하면서 다양한 툴을 익혔습니다. 또한 각 툴을 이용해서 자동화 스크립트를 개발하는 미니 프로젝트를 진행했습니다.
</div>
<div>
<br>
<h4>사용 기술 스택</h4>

<li>Ubuntu 18.04</li>
<li>Bash Shell</li>
<li>Crontab</li>
<li>Rsync</li>
<li>awk</li>

<h4>이런 걸 배웠어요</h4>

<li>Rsync를 이용한 원격서버와 로컬 연동 작업</li>
<li>Mysql dump 활용 DB 백업 및 Crontab을 이용한 업무 스케쥴링</li>
<li>Shell 문법 기반 자동화 스크립트 작성 경험</li>
<li>awk를 이용한 영화 목록 텍스트 데이터 및 로그 파일 분석</li>
</div>
</div>


## 피로그래밍(동아리)
--- 
<div class="grid-container">
<div class="left-container" style="margin-top:0rem;">

<h3>NearByCafe 웹 개발</h3>
<a href="https://github.com/minyou2675/NearByCafe">깃허브링크 
<img src="/images/github.png" alt="" width="30px" height="30px"></a>
<br>
개발기간 23.02 ~ 23.03
<br>Django 웹 개발 대학연합 동아리인 피로그래밍에서 5명의 팀원으로 카페 리뷰 홈페이지를 개발하였습니다.
</div>
<div>
<h4>사용 기술 스택</h4>
<li>JavaScript</li>
<li>Python</li>
<li>Django</li>

<h4>제가 맡은 역할</h4>
<li>세션을 이용한 사용자 로그인, 로그아웃 처리</li>
<li>검색 API 개발</li>
<li>Nginx로 서버 프록시 및 TLS 인증을 통한 Https 적용</li>
<li>EC2로 웹 사이트 배포작업</li>

<h4>이런 걸 배웠어요</h4>
<li>Django를 이용한 어플리케이션 구축</li>
<li>짧은 시간내 프로젝트를 완료하기 위한 팀원간 스프린트 경험</li>
<li>Github를 이용한 협업 경험</li>
<li>Ajax를 이용한 비동기 HTTP 통신 메소드 사용</li>
<li>MTV구조 개발 경험</li>
</div>
</div>

## UMC(동아리)
---
<div class="grid-container">
<div class="left-container" style="margin-top:0rem;">

<h3>독후감 커뮤니티 어플리케이션</h3>
<a href="https://github.com/minyou2675/TALER-SERVER">깃허브링크 
<img src="/images/github.png" alt="" width="30px" height="30px"></a>
<br>
개발기간 22.12 ~ 23.02
<br>
모바일 어플리케이션 개발에 대한 관심을 기반으로 UMC라는 연합동아리에서 활동하면서 독후감을 주제로한 모바일 어플리케이션의 백엔드 파트를 맡았습니다.
</div>
<div>

<h4>사용 기술 스택</h4>
<li>java 17</li>
<li>Spring Boot</li>

<h4>제가 맡은 역할</h4>
<li>백엔드(CRUD API 구현)</li>

<h4>이런 걸 배웠어요</h4>
<li>Spring Boot 프레임워크 사용 경험</li>
<li>DTO,DAO를 이용한 계층간 데이터 교환 구현</li>
<li>try문을 이용한 자원 관리와 해제 및 catch로 에러처리 구현</li>
<li>@RestController 기반 Restful Controller 구현</li>
</div>

</div>



## KT 산학 AI 경진대회
--- 
<div class="grid-container">
<div class="left-container" style="margin-top:0rem;">

<h3>AI기반 유기견 개체 인식 프로그램 개발</h3>
<a href="https://github.com/00ssum/KT-SMU-AI-project">깃허브링크 
<img src="/images/github.png" alt="" width="30px" height="30px"></a>
<br>개발기간 22.06 ~ 22.09
<br>4명의 팀으로 KT와 상명대학교 주관으로 주최한 AI경진대회에 참가하여 공익을 위한 유기견 개체 인식 프로그램을 기획 및 개발하여 최우수상을 수상하였습니다.

</div>
<div>
<h4>사용 기술 스택</h4>
<li>Python</li>
<li>Pytorch</li>
<li>AWS S3,RDS</li>

<h4>제가 맡은 역할</h4>
<li>YoloV5와 ResNet 기반 견종 객체인식 모듈 개발</li>
<li>모듈 통합 작업 진행</li>
<li>AWS RDS,S3 서비스 적용</li>

<h4>이런 걸 배웠어요</h4>
<li>객체인식 AI 서비스 기반 비디오 처리 기술</li>
<li>Python OpenCV 라이브러리를 이용하여 이미지 처리 경험</li>
</div>
</div>


<!-- ## PRESENTATIONS -->

## CERTIFICATES
---
AWS Solutions Architect Associate (2023.10)

SQLD (2022.09)

OPIC English IH(Intermediate High) (2023.03)

## AWARDS
---
KT 산학 AI 경진대회 최우수상(KT 이사장상,상명대학교 총장상)

SW인재페스티벌 우수상(소프트웨어중심대학협의회장상)

## ETC
---
미국 산호세 주립대학교 IT 연수
<br>2023.07 ~ 2023.08

대만 국립중앙대학교 교환학생
<br>2019.09 ~ 2020.02

육군 복무(의무병)
<br>2020.06 ~ 2021.12

(주)에스원 소프트웨어 테스트 아르바이트
<br>2020.03 ~ 2020.06

평택시청 행사과 아르바이트
<br>2019.01 ~ 2019.02

서울시청 세무과 아르바이트
<br>2018.12 ~ 2019.01
