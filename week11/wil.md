# 7주차 강의 요약
=================

## Relation과 FK
 **RDBMS** 
 - 관계형 데이터베이스 관리 시스템
 - PK : 기본 키, 구분자
   + 조건 : 고유한 값, 변경되지 않는 값, 모든 로우가 가지는 값 
 - fk : 외래 키
   + 다른 테이블의 정보를 참조하기 위한 값. 다른 테이블과의 관계를 표현해 줌.

 **관계**
 - 일대일 관계 
 - 일대다 관계 : '다'에 해당하는 테이블이 FK를 가짐
 - 다대다 관계 : 테이블 연결을 위해 2개의 FK만 모아둔 보조 테이블을 생성함(2개의 일대다 관계로 나눔)
 

## FK ORM
 **외래 키 생성** 
 - to, on_delete 파라미터 필수
   + on: 외래 키가 연결될 테이블을 구현한 Model 클래스
   + on_delete에 속성 지정 가능
     -  Models.CASCADE - 외래 키로 연결된 항목이 삭제되면 해당 항복도 같이 삭제함.
     -  Models.PROTECT - 
     -  Models.SET_NULL - fk 필드 값을 null로 바꿈(null=True 일 때만 사용 가능)
     -  Models.SET_DEFAULT - fk 필드 값을 default로 변경(default 값이 있을 때만 사용 가능)
     - Models.NOTHING - 아무런 행동 취하지 않음

 - 일대일 관계 - OneToOneField() 사용. (unique = True 속성과 동일)
 - 다대다 관계에서는 Models.ManyToManyField() 사용 
   + ManyToManyField("클래스이름")








