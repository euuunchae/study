# 10주차 강의 요약
=================

## Http Method(복습)


## ORM 심화 & 실습
 **장고 ORM 사용법** 
 - Question() - 객체 만들기, save() - 저장
 - Objects.create() - save() 과정 생략 가능

 **수정**
 - 저장되어 있는 값 가져와 수정하고 다시 저장
 - _실습_
  + 기존 detail.html 수정 - 수정, 삭제 만들기
  + 기존의 질문 내용이 보이도록! --> input 태그의 value 속성애 기존 질문 제목, 내용 넣어주기
  + templates - question_update.html 추가
 

 **삭제**
 - 저장되어 있는 값 가져와 delete() method 사용
 - _실습_
   + question_delete()함수 추가 - delete() method
   + 리다이렉트 시킴

   
 **검색**
 -  제목 및 내용에 검색어가 포함되어 있는 모든 질문 리스트 제공해야 함
 - | (or) 연산 이용 복잡한 쿼리




