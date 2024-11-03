# 5주차 강의 요약
=================


## Model과 ORM
 **Model**
- models.py에 클래스 생성 -> DB 테이블 생성
- DB 테이블에서 값 조회 시 models.py 클래스 객체에 값 담아 반환
- 클래스 == 과자 틀, 객체 == 과자

**장고 ORM 사용법**
- 클래스이름.objects.all() : _모든_ 테이블 정보를 객체로 만들어 리스트에 넣어 반환
- 클래스이름.objects.get() : _조건에 맞는_ 데이터를 객체로 만들어 반환
- 클래스이름.objects.filter() : _조건에 맞는_ 데이터들을 객체로 만들어 리스트에 넣어 반환


## 장고 template 문법
 **동적 html 생성** 
 - render(request, 'index.html', context)
 - request :  HTTP Request 객체
 - 'index.html' : 응답할 html 파일 이름
 - context : html 파일에서 사용할 딕셔너리(key값 문자열이어야 함) 
  + DB 정보 전달 시 'key.객체변수이름'으로 사용
  + ex <p>{{student.address}}</p>

 **HTML**
 - 웹페이지의 구조를 나타내는 마크업 언어. 태그 이용
 - 태그 종류
  + h1, h2, h3 : 제목 생성. 숫자 커질 수록 폰트 크기 작아짐
  + p : 문단 생성. 입력한 부분 앞 뒤로 빈 줄 생성
  + a : 하이퍼링크 
  + <span style="color:blue"> form, input </span> : 데이터를 입력받고 전송하기 위한 태그

 - CSS : 웹페이지를 꾸미기 위해 작성하는 코드(e.g. 색상) -> 프론트엔드 담당


## 실습
 **동적 html 생성해보기**
 - question만들어서 해당 DB 정보 전달하기
 **template 만들기**
 - 하이퍼링크 추가 시 urls.py에서는 path 추가, views.py에는 함수 추가


