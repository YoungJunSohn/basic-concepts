# SQL에서 DCL, DML, DDL 의 차이

<br/>

### SQL이란?

<br/>
SQL이란 Structured Query Language. 구조화 질의문의 약자로 관계형 데이터베이스 관리 시스템(RDBMS)의 데이터를<br/>
관리하기 위해 설계된 특수한 프로그래밍 언어이다.<br/>
<br/>
쉽게 말해 관계형 데이터베이스에서 한정적으로 사용되는 프로그래밍 언어라고 정의할 수 있다.<br/>
<br/>
SQL 문법에는 크게 세 가지 종류로 구분될 수 있는데 바로 *DDL* / *DML* / *DCL*이 바로 그것이다.<br/>
흔히 DB에서 말하는 CRUD는 모두 이 명령어들을 통해서 처리되고 실행된다.<br/>
<br/>
* DDL(Data Definition Language) : 데이터 정의 언어로, 스키마(schema)를 정의하거나 조작하기 위해 사용한다.<br/>
** schema란 데이터베이스의 구조와, 제약 조건에 관한 전반적인 명세를 기술한 메타데이터이다.<br/>
<br/>
* DML(Data Manipulation Language) : 데이터 조작 언어로, CRUD(생성,조회,수정,삭제)하기 위해 사용한다.<br/>
사용자가 응용 프로그램과 데이터베이스 사이에 실질적인 데이터 처리를 위해서 사용한다.<br/>
<br/>
* DCL(Data Control Language) : 데이터 제어 언어로, 데이터의 보안, 무결성, 회복, 병행수행제어 등을 정의하는데 사용한다.
** 데이터 무결성(data integrity)이란, 데이터의 정확성/일관성/유효성이 유지되는 것을 말한다.<br/>
<br/>