

<div align=center>
 
![여기어때 헤더](https://user-images.githubusercontent.com/86812173/155169218-edf5c234-9457-4433-a814-ecbcfee18ee8.png)
</div>

<h2>📌이민정 포트폴리오</h2>
<br>

### [포트폴리오](https://github.com/leeminjung/Yeogieottae-Clone/blob/master/%EC%9D%B4%EB%AF%BC%EC%A0%95%20%ED%8F%AC%ED%8A%B8%ED%8F%B4%EB%A6%AC%EC%98%A4.pdf) - 포트폴리오 PDF 주소
<br>



<h2>📌PROJECT OVERVIEW</h2>
 
> **<h3>숙박 예약 웹사이트인 "여기어때" 프로젝트</h3>**


코로나19 확산이 점점 가속화되어 실외보다는 실내위주의 생활을 찾게되면서 평소에 자주 이용하는 야놀자나 여기어때와 같은 숙박 예약 플랫폼을 만들어 보고 싶다는 생각이 들게 되어
팀원들과 회의 끝에 결정하게 되었다. <br>프로젝트에서는 기획PPT 작성 / 사용자페이지 : 메인화면 UI디자인, 회원가입, 비밀번호찾기, 이벤트, 확인문자전송 / 호스트페이지:이용규칙관리 / 관리자페이지: axios활용하여 연결 등 담당하여 구현해 나갔다. 

## 🛠 Tech STACK 🛠
<div align=center>
 <img src="https://img.shields.io/badge/JAVA-007396?style=flat-square&logo=java&logoColor=white">&nbsp
 <img src="https://img.shields.io/badge/HTML-E34F26?style=flat-square&logo=html5&logoColor=white">&nbsp 
 <img src="https://img.shields.io/badge/CSS-1572B6?style=flat-square&logo=css3&logoColor=white">&nbsp
 <img src="https://img.shields.io/badge/javascript-F7DF1E?style=flat-square&logo=javascript&logoColor=black">&nbsp
 <br>
 <img src="https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white">&nbsp
 <img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=flat-square&logo=spring boot&logoColor=white">&nbsp
 <img src="https://img.shields.io/badge/jQuery-0769AD?style=flat-square&logo=jquery&logoColor=white">&nbsp
 <img src="https://img.shields.io/badge/axios-512BD4?style=flat-square&logo=axios&logoColor=white">&nbsp
 <img src="https://img.shields.io/badge/Thymeleaf-005F0F?style=flat-square&logo=thymeleaf&logoColor=white">&nbsp
  <br>
</div>
<div align=center>
 <strong>프론트엔드 4명</strong><br>
 <strong>백엔드 2명</strong><br>
</div>


## 💭작업 기간💭
<br>

### 2021.07.20 ~ 11.01 

<br>
<br>

## 🖥️ 구현 화면 🖥️

### 1. 메인화면
 
 - 전체적으로 단순하고 밋밋한 UI ➡ <ins> 여기어때만의 색깔과 감성이 보여지는 확 트인 UI로 디자인후 변경 </ins>
 > 프로젝트를 만들고 있던 중에 문득 코로나19 확산으로 여행을 가지 못하는 사람들이 어디론가 떠나고 싶어하지 않을까? <br> 그런 마음을 가지고 웹사이트를 방문하는 사람들을 위로해줄 수 있는
  요소를 메인에 추가할 수 있는 방법을 없을까? 라는 아이디어가<br> 떠올라 여기어때 광고에 사용되고있는 선우정아 - '도망가자' BGM을 넣어 재미요소를 넣게 되었다. <br>
  또한 답답한 UI를 깔끔하게 새로 배치하고 구성하여 소비자들이 자주 찾고 즐겨볼 수 있도록 만들었다.   
 
<div align=center>
  
![ezgif com-gif-maker](https://user-images.githubusercontent.com/86812173/155129671-89e77c43-08d8-444c-b921-4b7bf6365688.gif)
  
</div>



### 2. 회원가입/로그인

 - 회원가입 및 로그인  ➡ <ins>휴대폰 인증을 통한 유효성검사와 랜덤닉네임 생성기를 통한 재미요소 추가 😊</ins>
 > SNS인증뿐만 아니라 세부적으로 맞다 틀리다를 보여줌으로써 회원가입과정을 매끄럽게 만들어주고, 닉네임 고민을 하는 사람들을 위한 
 <br>닉네임랜덤생성기로 회원가입시간을 단축시켜 편리하도록 하였다.

<div align= center>
 
 ![회원가입및로그인](https://user-images.githubusercontent.com/86812173/155985878-24b0cb18-1fb8-4100-8049-bf1750eaae8d.gif)

 </div>
 
 ----------
 ```js
 // 위 코드 생략
 // 이민정, 21.09.14
 // SMS인증번호 일치 확인 문구
            $(".checkcode").on("click", function () {
                if ($("#ucode").val() == code) { //  ucode : 사용자가 입력한 인증번호 , code: 발송된 인증번호
                    ($("#codeResult").html("일치합니다"));
                    chkSms = true;
                    clearInterval(timer); //인증확인 일치할경우 타이머멈추기
                    $('.time').html(""); //타이머 사라지게하기
                } else {
                    ($("#codeResult").html("일치하지 않습니다"));
                }
            })
 ```

### 3.찜하기
- <ins>기존 웹페이지에 없는 찜하기 기능과 찜목록 추가</ins>
> 찜을 하기위해 빈하트를 눌러주면 하트가 채워지면서 귀여운 효과를 보여줄수있다. 🤍 👉 ❤️ <br>
> 또한 찜목록을 추가하여 다시 보고싶은 숙소를 모아볼 수 있도록 만들었다. 

<div align= center>
 
![찜하기](https://user-images.githubusercontent.com/86812173/156002798-57a4cf6e-ca61-4b62-9e3c-f789355aa9c8.gif)

 </div>
 
 ### 3.호스트 페이지
 > 1. 사용자가 숙소를 예약하면 예약내역에 해당 숙소가 뜸 ( 여기서, 콘레드 호텔을 예약) <br>
 > 2. 호텔의 호스트 아이디로 로그인하여 호스트페이지를 들어가면 이전에 입력한 숙소정보들이 그대로 보여지고 각 페이지마다 수정가능 <br>
 > 3. 실시간예약관리에 그날 예약건수를 그래프로 쉽게 확인할 수 있다. <br>


 <div align= center>
 
 ![호스트](https://user-images.githubusercontent.com/86812173/156031892-565048bf-6308-47aa-8404-4b44f9463c8a.gif)
 
  </div>
  
  
  ### 4.관리자 페이지
  - <ins>사용자와 호스트 모두 관리할 수 있도록 구성</ins>
  > [  전체회원관리, 탈퇴회원관리, 전체호스트관리, 숙소관리, 리뷰관리, 예약/결제내역, 취소내역, 1:1문의관리, 결제시스템관리  ] <br>
  > 호스트회원이 숙소를 등록하면 관리자페이지에서 승인절차를 처리할수 있다. (대기 👉 승인) <br>
  > 알림을 통해 그날그날 처리되지않은 건수를 파악할 수 있다.
  
  
 <div align= center>
 
 ![admin_edit](https://user-images.githubusercontent.com/86812173/156308172-a37817b9-4e13-415e-802d-69d44f5533e4.gif)

 </div>
 
### 📑PROJECT REVIEW📑

> <strong>나를 성장시키는 경험</strong> <br>
> <br>
> 다른 팀과 다르게 비전공자들로만 이루어진 팀이라 하나부터 열까지 시작할때마다 걸려 넘어졌던것 같다. <br>
> 처음 주어진 한달 반이라는 시간에 모두들 밤낮을 매달려 구현해 냈지만 <strong>시행착오의 시간이 더 컸던지라</strong> 원하는 모습이 갖추어지지 않았고 결국 모든 팀이 기간을 연장했다.
> 다른 팀에 비해 조금 더 구현속도가 빨랐었지만 그것도 중간과정즈음엔 정체기를 맞이했다. 그것에 다들 많이 지치면서 갈등도 일어나고 팀을 나가시는 분도 계셨다. <br>
> 그러나 이러한 시간들을 직접 살로 맞닿아 겪다보니 극복하는 것 또한 오랜시간이 걸리진않았다. 남은 팀원들과 다시금 효율적인 방법을 모색해서 전체회의를 아침 저녁으로 하고
> <strong>필요한 정보공유나 공동작업 부분을 위해서는 24시간 하루 종일 회의도 마다하지 않았던것 같다.</strong> 메모장에 사용자, 호스트, 관리자 항목으로 나눠서 각자 파트를 맡아 진행하고 만들게되면
> to do list 항목 지우고 못끝내신 분들 도와드리는 방법으로 하니 속도가 엄청 빠르게 흘러갔다.
> 첫 프로젝트 완성을 하고 발표를 끝내니 후련하기도하고 복잡미묘한 감정이 들었던것같다! 😊😊    
> 

<div align= center>
 
![화면 캡처 2022-03-03 214247](https://user-images.githubusercontent.com/86812173/156567006-0f7319a4-cee0-4a4c-903c-28104ade261b.png)
 
 </div>


