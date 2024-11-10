# 6주차 강의 요약
=================


## Http Method
 - 해당 요청이 어떤 행동을 수행하는 메세지인지 전달하는 상태 코드
 - **Http request 구성**
    시작라인, 헤더, 공백 라인, 바디

 **GET**
 - 웹 브라우저의 기본 http method
 - url에 정보를 넣어 전달 (시작 라인)
 - 정보 읽기, 검색 요청에 주로 사용됨
 - 브라우저 캐싱 기능 지원

 _캐싱 가능한 요청_
   - 단순 조회를 요청하는 경우
   - 여러 번 요청해도 결과가 동일한 경우
   - url에 정보를 넣어 전달해도 되는 경우
 
 **POST**
 - 캐싱 기능X
 - request body에 정보 들어감
 - 새로운 요소 생성, 로그인 등에 사용됨
   
 _캐싱 불가능한 요청_
   - 요청마다 결과 변경이 가능한 경우
   - 민감한 정보를 다루는 경우
   - 새로운 리소스 생성을 요청하는 경우



## form 태그 및 사용법
 - input: type 속성을 이용해 입력 받을 데이터의 양식을 정할 수 있음
   - input type="submit" or <button>태그로 제출 버튼 만들기
 - form: action 속성에 지정한 링크로 입력받은 데이터 전송
   - form 안에 input 중첩 가능 -> 입력받기 가능
 - method 속성에 http method 지정 -> request message 맨 앞에 표시됨


## 추가 공부
 - **redirect를 사용하는 이유(PRG패턴)**
   - POST - Redirect - GET
   - POST method를 사용하는 경우, 새로고침 시 중복 발생 가능
   - 사용자: 웹 폼 작성, POST 방식으로 제출
   - 서버: 사용자를 다른 URL로 Redirect -> 사용자는 Redirect된 URL로 GET 방식 요청을 보냄

   -**장점**
     - 캐싱 가능(GET request), 새로고침 문제 해결, 북마크/공유 가능
   
 - **csrf**
   - Cross Stie Request Forgery: 사이트 간 요청 위조
   - 사용자가 악성 스크립트 페이지에 접근하도록 유도하여, 위조된 요청을 전송함. 이때, 웹 쿠키에 저장된 세션아이디를 함께 보냄으로써 서버가 해당 요청을 신뢰하게 함 
   - 악성코드가 서버에서 발생함
   - 방어 방법
     1. Referrer 검증
       - Http request header 정보에서 Referrer 정보 확인 -> host와 Referrer 값이 일치해야 함
     2. csrf token 사용
       - 사용자 세션에 임의의 값을 저장하여 모든 요청마다 해당 값을 포함하여 전송하도록 함
     3. CAPTCHA 사용
       - CAPTCHA 인증코드가 없거나 틀리면 요청 거부.
       - ex. 자전거 그림이 있는 타일을 고르시오..



